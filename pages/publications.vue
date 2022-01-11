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
                <div class="basis-1/3"> 
                    제목을 입력합니다.
                </div>   
                <div class="basis-2/3 max-w-6xl flex flex-col mt-5 md:mt-8 pb-14 md:pb-24 mx-auto px-6">
                    <div v-for="article of articles" :key="article">
                        <div :to='`article/${article.slug}`'>
                            <div class="flex justify-between items-center py-5 md:py-8 border-gray-600">
                                <div class="pr-4">
                                    <h2 class="mb-1 md:mb-1.5 text-lg md:text-xl font-medium poppins text-gray-800">{{ article.title }}</h2>
                                    <p class="mb-1 md:mb-1.5 text-sm md:text-sm text-gray-400">{{article.author}}</p>
                                    <p class="text-sm md:text-base text-gray-600 custom-text">{{article.description}}</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- else -->
        <div class="block md:hidden">
            <div class="max-w-6xl grid grid-cols-1 colspan mt-5 md:mt-8 pb-14 md:pb-24 max-w-6xl mx-auto px-6">
                <div class="group" v-for="article of articles" :key="article">
                    <div :to='`article/${article.slug}`'>
                        <div class="article-inner flex justify-between items-center py-5 md:py-8 border-gray-600">
                        <div class="pr-4">
                            <h2 class="mb-1 md:mb-1.5 text-lg md:text-xl font-medium poppins text-gray-800">{{ article.title }}</h2>
                            <p class="mb-1 md:mb-1.5 text-sm md:text-sm text-gray-400">{{article.author}}</p>
                            <p class=" text-sm md:text-base text-gray-600 custom-text">{{article.description}}</p>
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
    const articles = await $content('publications', params.id)
      .sortBy('createdAt', 'desc')
      .fetch();
    return {
      articles
    }
  },
}
</script>

<style scope>
</style>