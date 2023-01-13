<script setup lang="ts">
definePageMeta({
    // middlewear:"mymiddlewear.ts"
})

const {data: counter} = useFetch('/api/counter')

</script>

<template>
    <div>info about myself</div>
    <div>{{counter }}</div>
</template>