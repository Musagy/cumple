<script setup lang="ts">
import { ref } from 'vue'
const images = [
  'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRABMpvaA0j1qBw_w8G_r9FCQear0i6tORS2w&usqp=CAU',
  'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRERJwaAHy3T4UOGzGxxE6rgBYIVVyJZz65WuG650eOzpjCnfzPIEX_JUNuNkhHwYKFmxg&usqp=CAU'
]
const imgSrc = ref(images[0])
</script>

<template>
  <img :src="imgSrc" :alt="imgSrc" />
  <h1>¡¡¡feliz cumpleaños lucho!!!</h1>
  <img :src="imgSrc" alt="image" />
</template>

<style>
h1 {
  --size-border: 1px;
  font-size: 4rem;
  font-weight: 900;
  text-align: center;
  color: white;
  -webkit-text-stroke: 3px black;
  text-shadow:
    var(--size-border) var(--size-border) 0 #000,
    calc(var(--size-border) * -1) var(--size-border) 0 #000,
    calc(var(--size-border) * -1) calc(var(--size-border) * -1) 0 #000,
    var(--size-border) calc(var(--size-border) * -1) 0 #000;
}
img {
  animation: divertida 10s infinite;
  max-height: 230px;
  object-fit: contain;
}
@keyframes divertida {
  0% {
    transform: rotate(0deg);
  }
  25% {
    transform: rotate(360deg);
  }
  50% {
    transform: rotate(-180deg);
  }
  75% {
    transform: rotate(180deg);
  }
  100% {
    transform: rotate(-360deg);
  }
}
</style>
