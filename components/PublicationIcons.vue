<template>
    <div class="flex flex-row text-violet-400 text-sm">
        <div v-if="link" class="flex hover:text-violet-300 transition duration-200 items-center">
            <div class="pr-1"><Link /></div>
            <div class="pr-3"><a :href="`${journal.link}`" target="_blank">Link</a></div>
        </div>
        <div v-else></div>
        <div class="flex hover:text-violet-300 transition duration-200 items-center">
            <div class="pr-1"><Code /></div>
            <div class="pr-3"><a :href="`${journal.link}`" target="_blank">Code</a></div>
        </div>
        <div class="flex hover:text-violet-300 transition duration-200 items-center">
            <div class="pr-1"><Slide /></div>
            <div class="pr-3"><a :href="`${journal.link}`" target="_blank">Slides</a></div>
        </div>
        <div class="flex hover:text-violet-300 transition duration-200 items-center">
            <div class="pr-1"><Video /></div>
            <div class="pr-3"><a href="`${journal.link}`" target="_blank">Video</a></div>
        </div>
    </div>   
</template>

<script>

</script>
