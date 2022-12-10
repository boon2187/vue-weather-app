<!-- Reslut.vue -->

<template>
    <h2>気象データ</h2>
    {{ props.results }}
</template>

<script>
    const props = defineProps({
        results: Object
    })
</script>
