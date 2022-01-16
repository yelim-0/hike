<template>
  <div class="w-full">
    <div class="pt-16">
      
      <!-- 메인 문구 -->
      <!--if media query: -->
      <div class="px-14">
        <div class="hidden md:block">
            <div class="my-72 flex flex-row justify-center">
                <div class="w-68 h-60 pr-11 border-r-2">
                    <HikeLogo class="w-auto h-60"/>
                </div>
                <div class="w-auto py-8 pl-11">
                    <div class="text-gray-600 font-bold text-4xl md:mb-4">H I K E</div>
                    <div class="mt-5 md:mb-4 text-gray-600 font-semibold text-lg tracking-wider keepall">HYPER INTERLINKED<br> KNOWLEDGE ENGINEERING LABORATORY</div>
                    <div class="poppins text-gray-600">Department of Library and Information Science</div>
                    <div class="poppins text-gray-600">Chung-Ang University, Seoul, Korea</div>
                </div>
            </div>
        </div>
        <!--else:-->
        <div class="block md:hidden w-full">
            <div class="my-10 px-5 flex flex-col items-center">
                <div class="w-40 h-40 mb-10 mt-10">
                    <HikeLogo class="w-auto h-40" />
                </div>
                <div class="w-4/5 text-gray-600">
                    <div class="text-gray-600 font-semibold text-2xl text-center keepall mb-3">H I K E</div>
                    <div class="text-gray-600 font-medium text-lg text-center mb-3">HYPER INTERLINKED<br> KNOWLEDGE ENGINEERING LABORATORY</div>
                    <div class="text-sm text-center mt-3 poppins">Department of Library<br> and Information Science</div>
                    <div class="text-sm text-center mt-3 poppins">Chung-Ang University, Seoul, Korea</div>
                </div>
            </div>
        </div>
      </div>

      <!-- Research Subjects -->
      <div class="pt-16 md:pt-24 flex justify-center items-center max-w-6xl mx-auto px-6 pb-12 md:pb-16">
        <div class="text-xl md:text-4xl text-gray-600 text-center font-medium poppins pb-3 border-b-4 border-violet-400">Research Subjects</div>
      </div>

      <div class="max-w-6xl mx-auto px-6 pt-5 mb-16">
        
        <div class="hidden md:block px-20">
          <div class="grid grid-cols-2 gap-y-8 gap-x-14">
            <div class="research-box">
                <div class="p-5">
                  <h3 class="text-gray-700 text-lg font-bold keepall mb-2">Knowledge graph</h3>
                  <p class="text-sm md:text-base text-gray-500 mb-1">A knowledge graph is created by a significant endeavor. We study various techniques required to build large-scale data into knowledge graphs.</p>
                </div>
            </div>
            <div class="research-box">
                <div class="p-5">
                  <h3 class="text-gray-700 text-lg font-bold keepall mb-2">Data Science</h3>
                  <p class="text-sm md:text-base text-gray-500 mb-1">Data science is a method for inferring and gaining knowledge and insight from data. We understand large-scale data socially and scientifically and conduct various researches for problem solving.</p>
                </div>
            </div>
            <div class="research-box">
                <div class="p-5">
                  <h3 class="text-gray-700 text-lg font-bold keepall mb-2">Artificial Intelligence</h3>
                  <p class="text-sm md:text-base text-gray-500 mb-1">Artificial intelligence is a key technology for learning and processing data. We conduct various studies to understand text and analyze its meaning.</p>
                </div>
            </div>
            <div class="research-box">
                <div class="p-5">
                  <h3 class="text-gray-700 text-lg font-bold keepall mb-2">Data-driven Research</h3>
                  <p class="text-sm md:text-base text-gray-500 mb-1">We study the data. We study various perspectives of data to understand sociocultural phenomena and engineering studies on the creation and use of data.</p>
                </div>
            </div>
          </div>
        </div>

        <div class="block md:hidden hover:drop-shadow-lg">
            <div class="research-card">
              <div class="mb-4">
                <p class="text-base text-gray-700 font-bold pt-1 mb-2">Knowledge graph</p>
                <p class="text-gray-600 pt-1 mb-1">A knowledge graph is created by a significant endeavor. We study various techniques required to build large-scale data into knowledge graphs.</p>
              </div>
            </div>
            <div class="research-card">
              <div class="mb-4">
                <p class="text-base text-gray-700 font-bold pt-1 mb-2">Data Science</p>
                <p class="text-gray-600 pt-1 mb-1">Data science is a method for inferring and gaining knowledge and insight from data. We understand large-scale data socially and scientifically and conduct various researches for problem solving.</p>
              </div>
            </div>
            <div class="research-card">
              <div class="mb-4">
                <p class="text-base text-gray-700 font-bold pt-1 mb-2">Artificial Intelligence</p>
                <p class="text-gray-600 pt-1 mb-1">Artificial intelligence is a key technology for learning and processing data. We conduct various studies to understand text and analyze its meaning.</p>
              </div>
            </div>
            <div class="research-card">
              <div class="mb-4">
                <p class="text-base text-gray-700 font-bold pt-1 mb-2">Data-driven Research</p>
                <p class="text-gray-600 pt-1 mb-1">We study the data. We study various perspectives of data to understand sociocultural phenomena and engineering studies on the creation and use of data.</p>
              </div>
            </div>
        </div>
      </div>

      <!--Contact Us -->
      <div class="pt-16 md:pt-24 flex justify-center items-center max-w-6xl mx-auto px-6 pb-12 md:pb-16">
        <div class="text-xl md:text-4xl text-gray-600 text-center font-medium poppins pb-3 border-b-4 border-violet-400">Contact Us</div>
      </div>

      <div class="max-w-6xl mx-auto px-6 pt-5 mb-16">
        <div class="px-6 pt-10 pb-8 md:mx-20 rounded-lg w-auto h-auto bg-white shadow-xl ring-1 ring-gray-900/5">
          <div class="max-w-md mx-auto">
            <div class="md:py-8 text-base leading-7 space-y-6 text-gray-600">
              <ul class="space-y-4">
                <li class="flex items-center">
                  <p>
                    <span class="text-gray-700 text-lg font-semibold keepall pr-1">ADDRESS</span>
                    <span class="">1406, 303 Building, Chung-Ang University, 84 Heukseok-ro, Dongjak-gu, Seoul, Korea</span>
                  </p>
                </li>
                <li class="flex items-center">
                  <p>
                    <span class="text-gray-700 text-lg font-semibold keepall pr-1">EMAIL</span>
                    <span class="hover:underline"><a href="mailto:hike.lab@gmail.com">hike.cau@gmail.com</a></span>
                  </p>
                </li>
                <li class="flex items-center">
                  <p>
                    <span class="text-gray-700 text-lg font-semibold keepall pr-1">WEBSITE</span>
                    <span class="hover:underline"><a href="http://hike.cau.ac.kr">http://hike.cau.ac.kr</a></span>
                  </p>
                </li>
              </ul>
              <p class="keepall">Chung-Ang University is located in the heart of Seoul. Two subway lines link CAU with downtown Seoul. The subway stations near CAU are Sangdo Station on Line 7 and Heukseok Station on Line 9. By subway, downtown Seoul is 30 minutes away from CAU.</p>
            </div>
          </div>
        </div>

      </div>
      

    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>

<style scope>
.profile {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
.keepall{
    word-break: keep-all;
}

.research-box{
  @apply h-auto w-auto bg-white shadow-xl ring-1 ring-gray-900/5 rounded-lg;
}

.research-card{
  @apply rounded-lg h-auto py-5 px-6 mb-6 bg-white shadow-xl ring-1 ring-gray-900/5;
}

.featbox {
    width: 250px;
    height: 160px; 
    border-radius: 5%;
    overflow: hidden;
}

.back-purple {
  background-color: #E9E6EF;
}

</style>