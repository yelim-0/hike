<template>
    <div>
        <div class="pt-16 md:pt-44 flex justify-center items-center max-w-6xl mx-auto px-6">
            <div class="text-3xl md:text-4xl text-gray-800 font-medium poppins pb-3 border-b-4 border-violet-400">
                Publications
            </div>
        </div>

        <!-- publications list: Conference -->
        <!-- media query -->
        <div class="hidden md:block">
            <div class="flex flex-row">

                <div class="basis-1/3 mt-5 md:mt-8 pb-14 md:pb-24 mx-auto px-6 flex justify-end"> 
                    <div class="py-5 md:py-8 poppins text-base md:text-lg text-right text-violet-400 tracking-wider">International<br> Journal</div>
                </div>   

                <div class="basis-2/3 max-w-6xl flex flex-col mt-5 md:mt-8 pb-14 md:pb-24 mx-auto px-6">
                    <div v-for="journal of intJournals" :key="journal">
                        <div>
                            <div class="flex justify-between items-center py-5 md:py-8 border-gray-600">
                                <div class="pr-4">
                                    <h2 class="mb-1 md:mb-1.5 text-lg font-medium text-gray-800">{{ journal.title }}</h2>
                                    <p class="mb-1 md:mb-1.5 text-base text-gray-600">{{ journal.author }}</p>
                                    <p class="mb-1 md:mb-1.5 text-base text-gray-600 custom-text">{{ journal.description }}</p>
                                    <div class="flex flex-row text-violet-400 text-sm">
                                        <div class="flex hover:text-violet-300 transition duration-200 items-center">
                                            <div class="pr-1"><Link /></div>
                                            <div class="pr-3"><a :href="require(`${journal.link}`)" target="_blank">Link</a></div>
                                        </div>
                                        <div class="flex hover:text-violet-300 transition duration-200 items-center">
                                            <div class="pr-1"><Code /></div>
                                            <div class="pr-3"><a href="`${journal.Code}`" target="_blank">Code</a></div>
                                        </div>
                                        <div class="flex hover:text-violet-300 transition duration-200 items-center">
                                            <div class="pr-1"><Slide /></div>
                                            <div class="pr-3"><a href="`${journal.link}`" target="_blank">Slides</a></div>
                                        </div>
                                        <div class="flex hover:text-violet-300 transition duration-200 items-center">
                                            <div class="pr-1"><Video /></div>
                                            <div class="pr-3"><a href="`${journal.link}`" target="_blank">Video</a></div>
                                        </div>
                                    </div>    
                                </div>
                            </div>
                        </div>
                    </div>
                </div>



            </div>
        </div>

        <!-- else -->
        <div class="block md:hidden">
            <div class="max-w-6xl grid grid-cols-1 colspan mt-5 md:mt-8 pb-14 md:pb-24 mx-auto px-6">
                <div class="group" v-for="journal of intJournals" :key="journal">
                    <div :to='`article/${journal.slug}`'>
                        <div class="article-inner flex justify-between items-center py-5 md:py-8 border-gray-600">
                        <div class="pr-4">
                            <h2 class="mb-1 text-base font-medium poppins text-gray-800">{{ journal.title }}</h2>
                            <p class="mb-1 text-sm text-gray-600">{{journal.author}}</p>
                            <p class=" text-sm text-gray-600 custom-text">{{journal.description}}</p>
                        </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>




    </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const intJournals = await $content('publications', params)
      .sortBy('createdAt', 'desc')
      .fetch();
    return {
      intJournals
    }
  },
}
</script>

<style scope>
.custom-text {
    word-break: keep-all;
}
</style>