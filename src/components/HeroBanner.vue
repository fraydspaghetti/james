<script setup>
// Social Links - Update this links to your link
const FacebookLink = 'https://www.facebook.com/nogames231';



</script>

<template>
    <section class="flex flex-col justify-between gap-6 sm:gap-10 md:gap-16 lg:flex-row py-16">
        <!-- content - start -->
        <div class="flex flex-col justify-between xl:w-5/12">
            <div></div>

            <div class="sm:text-center lg:py-12 lg:text-left xl:py-24">
                <p class="mb-4 font-semibold text-gray-600 md:mb-6 md:text-lg xl:text-xl">Good Day!</p>

                <h1 class="mb-8 text-4xl font-bold text-cyan-700 sm:text-5xl md:mb-12">I'm James Alf Ochea your IT related works partner at your service.</h1>

                <div class="flex flex-col gap-2.5 sm:flex-row sm:justify-center lg:justify-start">
                    <router-link to="/contact" href="#"
                        class="inline-block rounded-lg bg-cyan-700 px-8 py-3 text-center text-sm font-semibold text-white outline-none 
                        ring-indigo-300 transition duration-100 hover:bg-cyan-600 focus-visible:ring active:bg-cyan-700 md:text-base">
                        About Me
                    </router-link>

                  

                 
                </div>
            </div>

            <!-- Social Media -->
            <div class="mt-8 flex items-center justify-center gap-4 sm:mt-16 lg:justify-start">
                <span class="text-sm font-semibold uppercase tracking-widest text-gray-400 sm:text-base">Facebook</span>
                <span class="h-px w-12 bg-gray-200"></span>

                <div class="flex gap-4">
                    <a :href="FacebookLink" target="_blank" 
                        class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600">
                        <svg class="h-5 w-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                            fill="currentColor" viewBox="0 0 8 19">
                            <path fill-rule="evenodd"
                                d="M6.135 3H8V0H6.135a4.147 4.147 0 0 0-4.142 4.142V6H0v3h2v9.938h3V9h2.021l.592-3H5V3.591A.6.6 0 0 1 5.592 3h.543Z"
                                clip-rule="evenodd" />
                        </svg>
                    </a>

                  

                 
                    
                </div>
            </div>
        </div>
        <div class="h-48 overflow-hidden rounded-lg bg-gray-100 shadow-lg lg:h-auto xl:w-5/12">
            <img src="../assets/james.jpg"
                loading="lazy" alt="MyPhoto" class="h-full w-full object-cover object-center" />
        </div>
    </section>
</template>