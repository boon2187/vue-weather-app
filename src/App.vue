<!-- // App.vue -->

<template>
  <Title />
  <Form @submit-form="getWeather" />
  <Results :results="results" />
</template>

<script setup>
import { reactive } from 'vue';
import axios from 'axios';
import Title from './components/Title.vue';
import Form from './components/Form.vue';
import Results from './components/Results.vue';

const results = reactive({
  country: "",
  cityName: "",
  temperature: "",
  conditionText: "",
  icon: ""
})

const getWeather = (city) => {
  axios.get(`http://api.weatherapi.com/v1/current.json?key=0be11468eae249b0b82234208221507&q=${city}&aqi=no`)
    .then(res => {
      results.country = res.data.location.country,
      results.cityName = res.data.location.name,
      results.temperature = res.data.current.temp_c,
      results.conditionText = res.data.current.condition.text,
      results.icon = res.data.current.condition.icon
    });
}
</script>
