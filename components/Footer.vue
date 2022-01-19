<template>
    <footer class="w-full bg-gray-50">
        <div class="max-w-6xl mx-auto pt-11 pb-14 md:pt-11 md:pb-24 px-2 md:px-5 border-t border-gray-300 flex flex-col md:flex-row items-center md:items-end justify-start md:justify-between">
            
            <!-- else -->
            <div class="md:hidden block flex flex-col px-3 text-base">
                <ul class="mb-1.5">
                    <li class="mb-3 font-medium text-gray-700 text-center">About</li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline text-sm text-center"><a href="/">HIKE</a></li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline text-sm text-center"><a href="http://bike.snu.ac.kr/" target="blank">BIKE</a></li>
                </ul>

                <ul class="mb-1.5">
                    <li class="mb-3 font-medium text-gray-700 text-center">Channels</li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline text-sm text-center"><a href="https://github.com/hike-lab" target="blank">GitHub</a></li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline text-sm text-center"><a href="http://discuss.datahub.kr">Discuss</a></li>
                </ul>

                <ul class="mb-1.5">
                    <li class="mb-3 font-medium text-gray-700 text-center">Collaboration</li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline text-sm text-center"><a href="http://okfn.kr/projects/covid-19-our-memory/" target="blank">Team.Cayley</a></li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline text-sm text-center"><a href="http://okfn.kr/" target="blank">Open Knowledge Korea</a></li>
                </ul>

                <ul class="mb-1.5">
                    <li class="mb-3 font-medium text-gray-700 text-center">External Links</li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline text-sm text-center"><a href="http://www.cau.ac.kr/" target="blank">Chung-Ang University</a></li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline text-sm text-center"><a href="http://lis.cau.ac.kr/" target="blank">Library and<br>Information Science</a></li>
                </ul>
            </div>    

            <div class="flex md:hidden justify-center items-center py-9">
                <HikeLogo class="w-10 h-10"/>
            </div>

            <!-- media query -->    
            <div class="hidden md:flex justify-around md:justify-start px-8 md:px-0 items-start">
                <ul class="ml-0 w-20 md:m-0">
                    <li class="mb-3 font-medium text-gray-700">About</li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline text-base"><a href="/" target="blank">HIKE</a></li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline text-base"><a href="http://bike.snu.ac.kr/" target="blank">BIKE</a></li>
                </ul>

                <ul class="w-28 md:ml-0 md:m-0">
                    <li class="mb-3 font-medium text-gray-700">Channels</li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline text-base"><a href="https://github.com/hike-lab" target="blank">GitHub</a></li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline text-base"><a href="http://discuss.datahub.kr">Discuss</a></li>
                </ul>

                <ul class="w-24 md:w-52 md:ml-0 md:m-0">
                    <li class="mb-3 font-medium text-gray-700">Collaboration</li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline text-base"><a href="http://okfn.kr/projects/covid-19-our-memory/" target="blank">Team.Cayley</a></li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline text-base"><a href="http://okfn.kr/" target="blank">Open Knowledge Korea</a></li>
                </ul>

                <ul class="w-24 md:w-44 md:ml-0 md:m-0">
                    <li class="mb-3 font-medium text-gray-700">External Links</li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline text-base"><a href="http://www.cau.ac.kr/" target="blank">Chung-Ang University</a></li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline text-base"><a href="http://lis.cau.ac.kr/" target="blank">Library and<br>Information Science</a></li>
                </ul>
            </div>

            <div>
                <div class="text-sm md:text-base text-gray-500 mt-3 md:mt-0 mb-3 text-center md:text-right">
                    ⓒ 2022 HIKE Lab. <br> All Rights Reserved.
                </div>
            </div>

        </div>
    </footer>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
</style>