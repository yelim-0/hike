<template>
    <div>
        <div class="pt-16 md:pt-44 flex justify-center items-center max-w-6xl mx-auto px-6">
            <div class="text-3xl md:text-4xl text-gray-800 font-medium poppins pb-3 border-b-4 border-violet-400">Director</div>
        </div>

        <div class="pt-12 md:pt-16 max-w-6xl mx-auto px-6 md:px-20">
            <div class="">
                <div v-for="leadm of Lead" :key="leadm">
                    <div class="max-x-3xl mx-auto md:flex md:justify-between md:items-center group">
                        <div class="flex justify-center">
                            <div class="lead-box w-40 h-40 mb-5 md:mb-0 md:w-52 md:h-52">
                                <img class="profile" :src="require(`~/assets/images/profile/${leadm.img}`)" alt="">
                            </div>
                        </div>
                        <div class="mx-auto pl-0 md:pl-12">
                            <div class="">
                                <div class="text-center md:text-left font-semibold text-lg md:text-xl poppins text-gray-800 group-hover:underline">{{leadm.name}}</div>
                                <div class="text-center md:text-left text-sm md:text-base poppins text-gray-800 mb-5">
                                    <a href="malito:haklaekim@gmail.com" class="hover:underline">haklaekim@gmail.com</a>
                                </div>
                                <div class="text-sm md:text-base poppins text-gray-800">
                                    Global Information Systems and Large-scale Data, specifically in the following area: 
                                    <ul>
                                        <li class="flex">
                                            <div class="pr-3 md:pr-5">•</div>
                                            <div>Knowledge Graph, including Data to Knowledge, Government Data and Open Data</div>
                                        </li>
                                        <li class="flex">
                                            <div class="pr-3 md:pr-5">•</div> 
                                            <div>Artificial Intelligence, including Machine Learning for Large-scale Data Processing</div>
                                        </li>
                                        <li class="flex">
                                            <div class="pr-3 md:pr-5">•</div> 
                                            <div>Data Science, including Large-scale Data Analytics and Visualizations</div>
                                        </li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="pt-16 md:pt-24 flex justify-center items-center max-w-6xl mx-auto px-6 pb-12 md:pb-16">
            <div class="text-3xl md:text-4xl text-gray-800 font-medium poppins pb-3 border-b-4 border-violet-400">Members</div>
        </div>

        <!-- members -->
        <div class="max-w-6xl mx-auto px-6 grid grid-cols-1 md:grid-cols-3 gap-x-3 md:gap-x-5 gap-y-9 pb-20 md:pb-24">
            <div v-for="imember of coreMember" :key="imember">
                <div class="flex justify-center mb-3 md:mb-5">
                    <div class="lead-box h-32 w-32 md:h-40 md:w-40">
                        <img class="profile" :src="require(`~/assets/images/profile/${imember.img}`)">
                    </div>
                </div>
                <div>
                    <div class="font-semibold text-lg md:text-xl text-center poppins text-gray-800 group-hover:underline">{{imember.name}}</div>
                    <div class="text-sm md:text-sm text-center poppins text-gray-800">{{imember.role}}</div>
                    <div class="text-sm md:text-sm text-center poppins text-gray-800">{{imember.email}}</div>
                    <div class="text-sm md:text-sm text-center poppins text-gray-800">{{imember.interests}}</div>
                </div>
            </div>
        </div>
        

    </div>
</template>

<script>
export default {
    async asyncData({ $content, params }) {
        const Lead = await $content('members', params.id)
        .where({role:'Director'})
        .fetch();
        const coreMember = await $content('members', params.id)
        .sortBy('name', 'asc')
        .where({role:'M.A.'})
        .fetch();
        return { coreMember, Lead }
    },
}
</script>

<style scoped>
.custom-text{
    word-break: keep-all;
}

.lead-box {
    border-radius: 70%;
    overflow: hidden;
}
.profile {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>
