<!-- Form.vue -->

<template>
    <form @submit.prevent="submitForm">
        <input type="text" v-model="city" placeholder="都市を英語で入力" />
        <button type="submit" >Get Weather</button>
    </form>
</template>

<script setup>
import { ref } from "vue";

const city = ref("");

const submitForm = () => {
    emits("submit-form");
}

// 上位コンポーネント（App.vue）にエミットする
const emits = defineEmits([
    "submit-form"
])
</script>
