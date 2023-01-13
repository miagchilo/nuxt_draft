<script setup lang="ts">
definePageMeta({
    // layout:"no-header"
})

const {data} = await useFetch("https://v2.jokeapi.dev/joke/Any?blacklistFlags=nsfw,explicit")
</script>
<template>
    <AboutText></AboutText>
    <img src="img/public_img.png" alt="">
    <img src="~assets/img/assets_img.png" alt="">
    <NuxtPage></NuxtPage>
    <div>{{ data }}</div>

</template>