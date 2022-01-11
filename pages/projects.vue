<template>
    <div>
        <div class="pt-16 md:pt-44 flex justify-center items-center max-w-6xl mx-auto px-6 mb-6 md:mb-12">
            <div class="text-3xl md:text-4xl text-gray-800 font-medium poppins pb-3 border-b-4 border-violet-400">Projects</div>
        </div>

        <div class="max-w-6xl mx-auto px-6 grid grid-cols-1 md:grid-cols-3 gap-x-5 gap-y-6 md:gap-y-6 pt-5 mb-20 md:mb-24">
      
            <div v-for="project of projects" :key="project" class="nthz hidden md:block hover:drop-shadow-lg transition duration-500">
                <div class="h-72 md:h-96 group">
                    <div class="h-3/5 flex items-center justify-center">
                        <div class="featbox">
                            <img class="featimg" :src="require(`~/assets/images/projects/${project.img}`)" alt="">
                        </div>
                    </div>
                    <div class="bg-white rounded-b-lg bg-opacity-75 group-hover:bg-violet-100 transition duration-200 h-2/5 p-5 z-30">
                        <p class="mb-1 md:mb-1 text-sm md:text-sm text-gray-500">{{project.category}}</p>
                        <h3 class="text-gray-800 poppins text-lg font-medium keepall mb-1">{{ project.title }}</h3>
                        <p class="text-sm md:text-sm text-gray-500">{{ project.description }}</p>
                    </div>
                </div>
            </div>

            <div v-for="project of projects" :key="project" class="block md:hidden hover:drop-shadow-lg">
                <div>
                    <div class="back-purple rounded-lg h-60 py-5 px-6 relative">
                        <div>
                            <p class="text-xs text-gray-500">{{ project.category }}</p>
                            <p class="text-base text-gray-700 font-bold pt-1 mb-2">{{ project.title }}</p>
                            <p class="text-gray-600 pt-1 ftmore mb-1">{{ project.description }}</p>
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
    const projects = await $content('projects', params.slug)
      .fetch();
  
    return {
      projects,
      
    }
  },
}
</script>

<style scope>
.nthz {
    @apply bg-white shadow-xl ring-1 ring-gray-900/5 rounded-lg;
}

.keepall{
    word-break: keep-all;
}
.bw{
  border: solid 1.8px #1f2937 ;
}
.featbox {
    width: 250px;
    height: 160px; 
    border-radius: 5%;
    overflow: hidden;
}
.featboxalt {
    width: auto;
    height: 230px; 
    border-radius: 0%;
    overflow: hidden;
}
.featimg {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
.back-yellow{
    background-color: #FBBF25;
}
.ftmore{
  font-size: 0.92rem;
}
</style>