<template>
  <div id="top">
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>

<script setup>
const title = ref("Sunbreak Hunting Attributes Calculator");
const description = ref("A fan-made tool to calculate the hunting attributes for MHR:Sunbreak.");
const keywords = ref("Monster Hunter, Monster Hunter Rise, Sunbreak, MHR, MHRS, MHR:S, 魔物獵人, 魔物獵人崛起, 魔物獵人崛起：破曉,モンスターハンターライズ, モンスターハンターライズ：サンブレイク, モンハン, モンハンライズ");

useHead({
  title,
  meta: [{
    name: "description",
    content: description
  }, {
    name: "keywords",
    content: keywords
  }],
  viewport: "width=device-width, initial-scale=1, maximum-scale=1",
  charset: "utf-8",
});
</script>