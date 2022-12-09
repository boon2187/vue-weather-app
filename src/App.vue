<!-- // App.vue -->

<template>
  <Title />
  <Form @submit-form="getWeather" />
</template>

<script setup>
import axios from 'axios';
import Title from './components/Title.vue';
import Form from './components/Form.vue';

const getWeather = () => {
  axios.get("http://api.weatherapi.com/v1/current.json?key=0be11468eae249b0b82234208221507&q=London&aqi=no")
    .then(res => console.log(res));
}
</script>
