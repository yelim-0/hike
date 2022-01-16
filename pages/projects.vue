<template>
    <div>
        <div class="pt-16 md:pt-44 flex justify-center items-center max-w-6xl mx-auto px-6 mb-6 md:mb-12">
            <div class="text-3xl md:text-4xl text-gray-800 font-medium poppins pb-3 border-b-4 border-violet-400">Projects</div>
        </div>

        <div class="max-w-6xl mx-auto px-6 grid grid-cols-1 md:grid-cols-1 gap-x-5 gap-y-6 md:gap-y-6 pt-5 mb-20 md:mb-24">
      
            <div v-for="project of projects" :key="project" class="nthz mb-5 hidden md:block">
                <div class="h-72 md:h-96 group flex flex-row px-10 py-6">
                    <div class="basis-1/4 flex justify-center items-center">
                        <div class="">
                            <img class="self-center" :src="require(`~/assets/images/projects/${project.img}`)" alt="">
                        </div>
                    </div>
                    <div class="basis-3/4 ml-9 bg-white rounded-b-lg bg-opacity-75 p-5">
                        <p class="mb-1 text-base text-gray-500">{{project.year}} | {{project.category}}</p>
                        <h3 class="mb-3 text-gray-800 poppins text-xl font-medium keepall">{{ project.title }}</h3>
                        <p class="text-sm md:text-base text-gray-600">{{ project.description }}</p>
                    </div>
                </div>
            </div>

            <div v-for="project of projects" :key="project" class="block md:hidden ">
                <div>
                    <div class="nthz h-72 py-5 px-6 relative">
                        <div>
                            <p class="text-xs text-gray-500">{{project.year}} | {{ project.category }}</p>
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
    const projects = await $content('projects', params)
        .sortBy('date', 'desc')
      .fetch();
  
    return {
      projects,
      
    }
  },
}
</script>

<style scope>
.nthz {
    @apply ring-1 bg-white drop-shadow ring-gray-900/5 rounded-lg;
}

.keepall{
    word-break: keep-all;
}
.bw{
  border: solid 1.8px #1f2937 ;
}

.back-yellow{
    background-color: #FBBF25;
}
.ftmore{
  font-size: 0.92rem;
}

.sbox {
  width: 212px;
  height: 141.33px;
  border-radius: 0.75rem;
  overflow: hidden;
}
.profile {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>