<script setup>
import Hero from "../components/Hero.vue";
import About from "../components/About.vue";

const name = "Ridwan Agung Ramadhan";
const job = "Web Developer";
const description =
  "Saya adalah seorang web developer yang baru terjun ke dunia pengembangan web dengan semangat dan antusiasme yang tinggi. Meskipun baru dalam industri ini, saya memiliki motivasi yang kuat untuk belajar dan berkembang menjadi seorang profesional web developer yang handal dan berkualitas.";
const image = "https://source.unsplash.com/1600x1500/?programming";


</script>

<template>
  <Hero :name="name" :job="job" :description="description" :image="image" />
  <About
  small-description=""
  description=""
  github="RidwanAR12"
  linkedin="ridwan-agung-ramadhan-79a382266"
  instagram="wan_ar12"
  />
</template>
