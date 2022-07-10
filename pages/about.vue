<template>
    <LHeader />
    <section class="bg-stone-800 text-white">
        <div class="line-before h-8 bg-cover"></div>
        <div class="container w-full md:max-w-7xl px-4 md:px-12 md:mx-auto py-16 flex flex-col gap-6">
            <div class="py-2">
                <h3 class="ttl-frame text-xl py-2 mb-4 mx-auto font-semibold tracking-wider text-center">SHAC
                </h3>
                <p>
                    Sunbreak Hunting Attributes Calculator (SHAC) is a calculator for optimising hunting based on the
                    weakeness
                    of the targeted mounsters.
                </p>
                <p>
                    SHAC uses nuxt 3 framework, check out the <a href="https://v3.nuxtjs.org" class="underline"
                        target="_blank" rel="noopener">nuxt 3 documentation</a> to learn more.
                </p>
            </div>
            <div class="py-2">
                <h3 class="ttl-frame text-xl py-2 mb-4 mx-auto font-semibold tracking-wider text-center">
                    Sauce
                </h3>
                <p>The data figures SHAC used are derived from ShawnW1031's work, available at
                    <a href="https://forum.gamer.com.tw/C.php?bsn=5786&snA=165373" class="underline" target="_blank"
                        rel="noopener">gamer.com.tw</a>
                    and
                    <a href="https://www.ptt.cc/MH/M.1657188036.A.A28" class="underline" target="_blank"
                        rel="noopener">PTT</a>. A big hand to him and <a
                        href="https://gamewith.jp/mhrize/article/show/312232" class="underline" target="_blank"
                        rel="noopener">gamewith.jp</a>!
                </p>
            </div>
            <div class="py-2">
                <h3 class="ttl-frame text-xl py-2 mb-4 mx-auto font-semibold tracking-wider text-center">Legal (kind of)
                </h3>
                <p>
                    "Monster Hunter" and "Monster Hunter Rise: Sunbreak" are registered trademarks or trademarks of
                    CAPCOM
                    CO., LTD.
                </p>
                <p>"モンスターハンターライズ" 及び "モンスターハンターライズ：サンブレイク"は株式会社カプコンの登録商標または商標です。</p>
            </div>
        </div>
        <div class="line-after h-8 bg-cover"></div>
    </section>
    <LFooter />
</template>

<style>
.ttl-frame {
    background: url(/img/capcom/sec-ttl_bg.png) center no-repeat;
    background-size: 100%;
    width: 30%;
}


.line-before {
    background-image: url(/img/capcom/top-line-img.png);
}

.line-after {
    background-image: url(/img/capcom/bottom-line-img.png);
}
</style>