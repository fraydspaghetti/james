<template>
    <div class="bg-white py-6 sm:py-8 lg:py-48">
        <div class="flex flex-wrap lg:flex-nowrap items-center justify-between gap-4 lg:gap-8 mb-8 md:mb-12">
            <div class="flex flex-col gap-2">
                <h2 class="text-2xl font-bold text-gray-800 lg:text-3xl">My Works</h2>

                <p class="text-gray-500 text-lg">
This are my recent works                </p>
            </div>

            
        </div>
        
        <!-- Project Image Gallery -->
        <div class="grid grid-cols-1 gap-4 md:grid-cols-3 md:gap-6 xl:gap-8">
            <!-- image - start -->
            <router-link to="/todolist" href="#" class="group relative flex h-48 items-end overflow-hidden rounded-lg bg-gray-100 shadow-lg md:h-80">
                <img src="../assets/todoapp.jpg"
                    loading="lazy" alt=""
                    class="absolute inset-0 h-full w-full object-cover object-center transition duration-200 group-hover:scale-110" />

                <div
                    class="pointer-events-none absolute inset-0 bg-gradient-to-t from-gray-800 via-transparent to-transparent opacity-50">
                </div>

                <span class="relative ml-4 mb-3 inline-block text-sm text-white md:ml-5 md:text-lg">TODO LIST APP</span>
            </router-link>
            <!-- image - end -->

            <!-- image - start -->
            <router-link to="/games"
                class="group relative flex h-48 items-end overflow-hidden rounded-lg bg-gray-100 shadow-lg md:col-span-2 md:h-80">
                <img src="../assets/games.jpg"
                    loading="lazy" alt="chatapp"
                    class="absolute inset-0 h-full w-full object-cover object-center transition duration-200 group-hover:scale-110" />

                <div
                    class="pointer-events-none absolute inset-0 bg-gradient-to-t from-gray-800 via-transparent to-transparent opacity-50">
                </div>

                <span class="relative ml-4 mb-3 inline-block text-sm text-white md:ml-5 md:text-lg">VUE APP</span>
            </router-link>
            <!-- image - end -->

            <!-- image - start -->
           
            <!-- image - end -->

            <!-- image - start -->

            <!-- image - end -->
        </div>
    </div>
</template>