<!-- Reslut.vue -->

<template>
    <div>{{ results.country }}</div>
    <div>{{ results.cityName }}</div>
    <div>{{ results.temperature }}</div>
</template>

<script setup>
    const props = defineProps({
        results: Object
    })
</script>
