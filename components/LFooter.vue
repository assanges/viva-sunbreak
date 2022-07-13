<template>
    <footer class="bg-zinc-900">
        <div class="relative max-w-screen-xl px-4 py-16 mx-auto sm:px-6 lg:px-8 lg:pt-24">
            <div class="absolute top-4 sm:top-6 lg:top-8 right-4 sm:right-6 lg:right-8">
                <a class="inline-block p-2 text-amber-300/75 bg-zinc-700 rounded-full sm:p-3 lg:p-4 hover:bg-zinc-500"
                    href="#top">
                    <span class="sr-only">Back to top</span>

                    <svg xmlns="http://www.w3.org/2000/svg" class="w-8 h-8" viewBox="0 0 20 20" fill="currentColor">
                        <path fill-rule="evenodd"
                            d="M14.707 12.707a1 1 0 01-1.414 0L10 9.414l-3.293 3.293a1 1 0 01-1.414-1.414l4-4a1 1 0 011.414 0l4 4a1 1 0 010 1.414z"
                            clip-rule="evenodd" />
                    </svg>
                </a>
            </div>

            <div class="lg:flex lg:items-end lg:justify-between">
                <div>
                    <div class="flex justify-center  lg:justify-start">
                        <img src="/img/capcom/elem_pt.png" class="h-32 w-32" fill="currentColor" />
                    </div>

                    <p class="max-w-md mx-auto mt-6 leading-relaxed text-center text-white lg:text-left font-serif">
                        Sunbreak Hunting Attributes Calculator
                    </p>
                </div>

                <nav class="mt-12 lg:mt-0" aria-labelledby="footer-navigation">
                    <h2 class="sr-only" id="footer-navigation">Footer navigation</h2>

                    <ul class="flex flex-wrap justify-center gap-6 lg:justify-end md:gap-8 lg:gap-10">
                        <li>
                            <a class="text-white hover:text-white/75" href="/">
                                Calculator
                            </a>
                        </li>
                        <li>
                            <a class="text-white hover:text-white/75" href="/about">
                                About
                            </a>
                        </li>
                        <li>
                            <a class="text-white hover:text-white/75" href="https://github.com/assanges/viva-sunbreak"
                                target="_blank" rel="noopener">
                                GitHub Repo
                            </a>
                        </li>
                        <li>
                            <a class="text-white hover:text-white/75"
                                href="https://www.monsterhunter.com/rise-sunbreak/" target="_blank" rel="noopener">
                                Monster Hunter Rise: Sunbreak
                            </a>
                        </li>
                    </ul>
                </nav>
            </div>

            <p class="mt-12 text-xs text-center text-gray-500 lg:text-right flex flex-col">
                <span class="flex-1 my-1 md:mr-3">
                    "Monster Hunter" and "Monster Hunter Rise: Sunbreak" are registered trademarks or trademarks of
                    CAPCOM
                    CO., LTD.
                </span>
                <span class="flex-1 my-1">"モンスターハンターライズ" 及び "モンスターハンターライズ：サンブレイク"は株式会社カプコンの登録商標または商標です。</span>
            </p>
        </div>
    </footer>
</template>