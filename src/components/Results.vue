<!-- Reslut.vue -->

<template>
    <div>{{ results.country }}</div>
    <div>{{ results.cityName }}</div>
    <div>{{ results.temperature }}</div>
    <div>
        <img :src="results.icon" alt="" />
        <span>{{ results.condtionText }}</span>
    </div>
</template>

<script setup>
    const props = defineProps({
        results: Object
    })
</script>
