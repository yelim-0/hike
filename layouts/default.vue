<template>
  <div class="absol bg-gray-50">
    <!-- <Header /> -->
    <Header class="fixed px-0 md:px-5" />
    <Nuxt class="bg-gray-50 px-0 md:px-5"/>
    <!-- <Footer /> -->
    <Footer class="px-0 md:px-6"/>
  </div>
</template>

<script>
export default {
  name: 'Default',
}
</script>

<style>
@import url(../assets/css/fonts.css);

.poppins{
    font-family: 'Poppins', 'Spoqa Han Sans', 'Inter';
  }

.absol{
    position: relative;
  }

.fixed{
    position: fixed;
  }

</style>