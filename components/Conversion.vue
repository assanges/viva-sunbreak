<template>
    <div class="container w-full md:max-w-6xl mx-auto">
        <div>
            <select
                class="inline-block w-full px-4 py-2 text-sm text-white border border-red-400 focus:ring-red-400 focus:border-red-400 bg-zinc-700 placeholder-gray-400 transition ease-in-out"
                aria-label="Language" v-model="locale">
                <option :value="item.value" v-for="item in localeList">
                    {{ item.text }}
                </option>
            </select>
        </div>
        <div class="overflow-x-auto">
            <table id="conversion-table" class="w-full text-md text-left">
                <thead class="text-md bg-stone-400/50 text-[#3d0a07]">
                    <tr>
                        <th scope="col" colspan="2" class="px-1 py-3 mx-auto text-center tracking-wide">MONSTER</th>
                        <th scope="col" class="px-2 py-3 mx-auto text-center" v-for="blights of conversion.blights">
                            <span>{{ blights[locale] }}</span>
                        </th>
                    </tr>
                </thead>
                <tbody>
                    <tr class="py-3">
                        <th class="py-2 text-center" colspan="2">
                            <div class="inline-block bg-yellow-400/50 text-lg rounded-full px-4 p-1 mr-1 md:mr-4">
                                <abbr :title="recommendationAbbr.first[locale]">1</abbr>
                            </div>
                            <div class="inline-block bg-gray-300/50 text-lg rounded-full px-4 p-1">
                                <abbr :title="recommendationAbbr.second[locale]">2</abbr>
                            </div>
                        </th>
                        <th class="px-2 text-center" v-for="recommend of recommendationBySelected"
                            :class="recommendedColour(recommendationBySelected)[0] === recommend ? ' bg-yellow-400/50' : recommendedColour(recommendationBySelected)[1] === recommend ? ' bg-gray-300/50' : ' bg-amber-900/25'">
                            <span>{{ recommend }}</span>
                        </th>
                    </tr>
                    <tr v-for="(properties, name, index) in conversion.effectivenessByMonster"
                        class="text-md text-[#3d0a07] items-center">
                        <td class="text-center items-center p-1">
                            <input type="checkbox" :id="name" v-model="selectedMonsters" :value="name"
                                @change="updateSuggestion"
                                class="w-4 h-4 text-orange-500 bg-gray-300/75 rounded border-gray-300 focus:ring-orange-800 focus:ring-2">
                            <label :for="name" class="sr-only">Select this monster</label>
                        </td>
                        <th class="text-sm inline-block tracking-wider">
                            {{ conversion.monsters[locale][index] }}
                        </th>
                        <td v-for="figures in properties" class="text-center">
                            {{ figures }}
                        </td>
                    </tr>
                    <tr class="my-8">
                        <td class="py-4"></td>
                    </tr>
                </tbody>
            </table>
        </div>

    </div>
</template>

<script setup>
import { ref } from "vue";
import conversion from "~/assets/conversion.json";

const defaultLocale = "zh";
const locale = ref(defaultLocale);
const localeList = ref([{
    value: "en",
    text: "English"
}, {
    value: "ja",
    text: "日本語"
}, {
    value: "zh",
    text: "中文"
}]);

const recommendationAbbr = {
    first: { en: "1st Best", zh: "第一", ja: "最適" },
    second: { en: "Next Best", zh: "第二推薦", ja: "代案" }
};

const selectedMonsters = ref([]);
const recommendationBySelected = ref([]);

const updateSuggestion = () => {
    const selected = selectedMonsters.value;
    let selectedFigures = [];

    // map figures by selected monsters 
    selected.map(name => {
        selectedFigures = selectedFigures.concat([conversion.effectivenessByMonster[name]]);
    });
    selectedFigures.length !== 0
        ? recommendationBySelected.value = selectedFigures.reduce(sumFigures)
        : recommendationBySelected.value = null;
};

//- https://stackoverflow.com/questions/32139773
const sumFigures = (r, a) => r.map((b, i) => a[i] + b);

const recommendedColour = (r) => {
    let max = Math.max(...r.map((i) => i));
    let negIfinity = -Infinity, secondMax = -Infinity;

    for (const value of r) {
        const nr = Number(value)

        if (nr > negIfinity) {
            [secondMax, negIfinity] = [negIfinity, nr] // save previous max
        } else if (nr < negIfinity && nr > secondMax) {
            secondMax = nr; // new second biggest
        }
    }
    return [max, secondMax];
};
</script>

<style>
#conversion-table::before {
    z-index: -5;
    content: "";
    background: url(/img/capcom/product_bg-t.jpg) center top no-repeat;
    background-size: 100%;
    top: 0;
    left: 0;
    right: 0;
    width: 100%;
    height: 20vw;
    display: block;
    position: absolute;
}

#conversion-table::after {
    content: "";
    z-index: -5;
    background: url(/img/capcom/product_bg-b.jpg) center bottom no-repeat;
    background-size: 100%;
    bottom: 0;
    left: 0;
    right: 0;
    width: 100%;
    height: 16vw;
    display: block;
    position: absolute;
}

#conversion-table {
    z-index: 10;
    position: relative;
    overflow: hidden;
    background: url(/img/capcom/product_bg-c.jpg);
    background-size: 100% auto;
    background-repeat: repeat-y;
    color: #3d0a07;
    padding: 3.2vw 2.4vw;
    width: 100%;
}

input[type='checkbox'] {
    -webkit-appearance: none;
    width: 30px;
    height: 30px;
    border-radius: 5px;
    border: 2px solid #555;
    vertical-align: middle;
}

input[type='checkbox']:checked {
    background: url(/img/capcom/icon_astrsk.png) no-repeat;
    background-position: center;
    display: inline-block;
    background-size: 90%;
}

abbr[title] {
    @apply relative underline decoration-dotted;
}

abbr[title]:hover::after,
abbr[title]:focus::after {
    content: attr(title);

    @apply absolute w-auto px-2 py-1 left-0 bottom-8 text-sm tracking-wider rounded bg-stone-800 text-white shadow whitespace-nowrap;
}
</style>