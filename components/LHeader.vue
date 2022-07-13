<template>
    <header class="bg-zinc-800">
        <div class="max-w-screen-xl px-4 py-2 mx-auto sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                <div class="flex-1 md:flex md:items-center md:gap-12">
                    <a class="flex gap-x-4 text-amber-300" href="/">
                        <span class="sr-only">Home</span>
                        <img src="/img/capcom/icon_sunbreak_alt.png" class="h-12 w-12" fill="currentColor" />
                        <h1 class="text-xl md:text-3xl font-semibold self-center uppercase tracking-widest">SHAC</h1>
                    </a>
                </div>

                <div class="md:flex md:items-center md:gap-12">
                    <!-- <nav class="hidden md:block" aria-labelledby="header-navigation">
                        <h2 class="sr-only" id="header-navigation">Header navigation</h2>

                        <ul class="flex items-center gap-6 text-sm">
                            <li>
                                <a class="text-white hover:text-white/75" href="/">
                                    Hunting Attributes Calculator
                                </a>
                            </li>

                            <li>
                                <a class="text-white hover:text-white/75" href="/about">
                                    About
                                </a>
                            </li>
                        </ul>
                    </nav> -->

                    <div class="flex items-center gap-4">

                        <div class="kare">
                            <a class=" px-4 py-2 inline-block text-base md:text-lg font-semibold text-amber-300 border-2 border-amber-300 bg-transparent hover:text-black hover:bg-amber-600 shadow"
                                href="https://www.youtube.com/watch?v=flQQmeKBEl0" target="_blank" rel="noopener">
                                <span class="inline-block">狩れ！</span>
                                <span class="inline-block ml-2"><img src="/img/capcom/buy-arrow.png" class="w-2" /></span>
                            </a>
                        </div>

                        <!-- to be implemented
                            <div class="block md:hidden">
                            <button class="p-2 text-white transition bg-gray-800 hover:text-white/75">
                                <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5" fill="none" viewBox="0 0 24 24"
                                    stroke="currentColor" stroke-width="2">
                                    <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
                                </svg>
                            </button>
                        </div> 
                        -->
                    </div>
                </div>
            </div>
        </div>
        <div class="block"></div>
    </header>
</template>