<template>
    <div class="w-full bg-gray-50 z-40">
        <div class="mx-auto flex items-center justify-between px-4">
            
            <div class="ml-0 md:ml-0 flex w-full pt-4">
                <nuxt-link to="/">
                    <!--<HikeHeaderLogo />-->
                </nuxt-link>
            </div>

            <div class="md:hidden flex content-center pt-4">
                <button @click="drawer">
                <Menu class="mr-0.5"/>
                </button>
            </div>

            <div class="flex hidden md:block py-5">
                <ul class="flex space-x-6 text-base items-center">
                    <li class="hidden md:block text-gray-500 pl-3 hover:text-gray-800 transition hover:duration-300 font-light">
                        <nuxt-link :to="{path: '/'}" replace class="poppins">Home</nuxt-link>
                    </li>
                    <li class="hidden md:block text-gray-500 hover:text-gray-800 transition hover:duration-300 font-light">
                        <nuxt-link :to="{path: '/people'}" replace class="poppins">People</nuxt-link>
                    </li>
                    <li class="hidden md:block poppins text-gray-500 hover:text-gray-800 transition hover:duration-300 font-light">
                        <nuxt-link :to="{path: '/projects'}" replace class="poppins">Projects</nuxt-link>
                    </li>
                    <li class="hidden md:block poppins text-gray-500 hover:text-gray-800 transition hover:duration-300 font-light">
                        <nuxt-link :to="{path: '/publications'}" replace class="poppins">Publications</nuxt-link>
                    </li>
                </ul>
            </div>

            <transition
                enter-class="opacity-0"
                enter-active-class="ease-out transition-medium"
                enter-to-class="opacity-100"
                leave-class="opacity-100"
                leave-active-class="ease-out transition-medium"
                leave-to-class="opacity-0"
            >
                <div @keydown.esc="isOpen = false" v-show="isOpen" class="z-10 fixed inset-0 transition-opacity">
                    <div @click="isOpen = false" class="absolute inset-0 bg-black opacity-50" tabindex="0"></div>
                </div>
            </transition>

            <aside class="p-5 transform top-0 left-0 w-64 bg-gray-50 fixed h-full overflow-auto ease-in-out transition-all duration-300 z-30" :class="isOpen ? 'translate-x-0' : '-translate-x-full'">
                
                <div class="close">
                <button class="absolute top-0 right-0 mt-4 mr-4" @click=" isOpen = false">
                    <Close />
                </button>
                </div>

                <div @click="isOpen = false" class="flex w-full pt-12 pb-8 items-center justify-center border-b">
                    <HikeLogo class="w-auto h-10" />
                </div>

                <ul class="divide-y font-light">
                    <li><nuxt-link :to="{path: '/'}" replace @click="isOpen = false" class="text-gray-500 my-4 inline-block poppins">Home</nuxt-link></li>
                    <li><nuxt-link :to="{path: '/people'}" replace @click="isOpen = false" class="text-gray-500 my-4 inline-block poppins">People</nuxt-link></li>
                    <li><nuxt-link :to="{path: '/projects'}" replace @click="isOpen = false" class="text-gray-500 my-4 inline-block poppins">Projects</nuxt-link></li>
                    <li><nuxt-link :to="{path: '/publications'}" replace @click="isOpen = false" class="text-gray-500 my-4 inline-block poppins">Publications</nuxt-link></li>
                </ul>

            </aside>
        </div>
    </div>
</template>

<script>
    export default {
    data() {
        return {
        isOpen: false
        };
    },
    methods: {
        drawer() {
        this.isOpen = !this.isOpen;
        }
    },
    watch: {
        isOpen: {
        immediate: true,
        handler(isOpen) {
            if (process.client) {
            if (isOpen) document.body.style.setProperty("overflow", "hidden");
            else document.body.style.removeProperty("overflow");
            }
        }
        }
    },
    mounted() {
        document.addEventListener("keydown", e => {
        if (e.keyCode == 27 && this.isOpen) this.isOpen = false;
        });
    }
    };
</script>

<style scoped>
</style>