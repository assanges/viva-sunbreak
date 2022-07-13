<template>
    <LHeader />
    <section class="bg-stone-800 text-white">
        <div class="line-before h-8 bg-cover"></div>
        <div class="container w-full md:max-w-5xl px-4 md:px-12 md:mx-auto py-16 flex flex-col gap-6">
            <div class="py-2">
                <h3 class="ttl-frame">About SHAC</h3>
                <div class="flex flex-col gap-y-4">
                    <p>
                        Sunbreak Hunting Attributes Calculator (SHAC) is a calculator for optimising hunting based on
                        the weakeness of the targeted mounsters.
                    </p>
                    <p>
                        Good Hunting! 良い狩りを！
                    </p>
                    <p>
                        SHAC is scaffolded with nuxt 3 framework, check out the <a href="https://v3.nuxtjs.org"
                            class="underline" target="_blank" rel="noopener">nuxt 3 documentation</a> to learn more.
                    </p>
                </div>
            </div>
            <div class="py-2">
                <h3 class="ttl-frame"><s>Sauce</s> Source</h3>
                <div class="flex flex-col gap-y-4">
                    <p>The data figures SHAC used are derived from Shawn's collation, available at
                        <a href="https://forum.gamer.com.tw/C.php?bsn=5786&snA=165373" class="underline" target="_blank"
                            rel="noopener">gamer.com.tw</a> (ShawnW1031)
                        and
                        <a href="https://www.ptt.cc/bbs/MH/M.1657188036.A.A28.html" class="underline" target="_blank"
                            rel="noopener">PTT/MH</a> (GaARo). A big hand to him for his hard work and original data from
                        <a href="https://gamewith.jp/mhrize/article/show/312232" class="underline" target="_blank"
                            rel="noopener">gamewith.jp</a>!
                    </p>
                </div>
            </div>
            <div class="py-2">
                <h3 class="ttl-frame">Privacy</h3>
                <div class="flex flex-col gap-y-4">
                    <p>
                        SHAC does not collect any information, SHAC is merely a calculator calculate best fit weapon for
                        hunting in Monster Hunter Rise: Sunbreak.
                    </p>
                </div>
            </div>
            <div class="py-2">
                <h3 class="ttl-frame">Legal (kind of)</h3>
                <div class="flex flex-col gap-y-4">
                    <p>
                        SHAC is a not-for-profit fan-made tool, which is not officially sponsored or supported by, or
                        affiliated with with CAPCOM.
                    </p>
                    <p>
                        All the third parties’ intellectual property, including trademarks, logos, and designs used
                        in this site are owned by their respective right holders.
                    </p>
                    <p>
                        "Monster Hunter" and "Monster Hunter Rise: Sunbreak" are registered trademarks or trademarks of
                        CAPCOM
                        CO., LTD.
                    </p>
                    <p>"モンスターハンターライズ" 及び "モンスターハンターライズ：サンブレイク"は株式会社カプコンの登録商標または商標です。</p>
                </div>
            </div>
            <img src="/img/capcom/privilege_ic.png" class="w-full md:w-1/3 place-self-center" />
        </div>
        <div class="line-after h-8 bg-cover"></div>
    </section>
    <LFooter />
</template>

<style>
.ttl-frame {
    background: url(/img/capcom/sec-ttl_bg.png) center no-repeat;
    background-size: 100%;
    width: 100%;
    @apply text-xl py-4 mb-8 mx-auto font-semibold tracking-wider text-center
}


@media only screen and (min-width: 768px) {
    .ttl-frame {
        background: url(/img/capcom/sec-ttl_bg.png) center no-repeat;
        background-size: contain;
        width: 40%;
        @apply text-xl py-4 mb-8 mx-auto font-semibold tracking-wider text-center
    }
}

.line-before {
    background-image: url(/img/capcom/top-line-img.png);
}

.line-after {
    background-image: url(/img/capcom/bottom-line-img.png);
}
</style>