<script setup lang="ts">
type AlertBoxTypes = "error" | "warning" | "success"


const props = defineProps<{
    type: AlertBoxTypes;
}>()


</script>


<template>
    <div :class="{red: type === 'error'}"
    >
        this is an alert box!
        <slot></slot>
    </div>
</template>

<style scoped>
.red {
    color: red;
}

.blue {
    color: blue;
}
</style>