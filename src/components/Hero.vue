<script setup>
const props = defineProps({
  name: String,
  job: String,
  description: String,
  image: String,
});
</script>

<template>
  <div
    class="container d-flex align-items-center justify-content-center"
    style="height: 100vh; height: 100vh">
    <div class="row d-flex align-items-center items-centers">
      <div class="col-md-6 d-grid gap-3" style="max-width: 50rem">
        <h1 class="fw-bold" style="font-size: 8rem" v-html="props.name" />
        <h4>{{ props.job }}</h4>
        <p align="justify">
          {{ props.description }}
        </p>
      </div>
      <div class="col-md-6">
        <!-- make image dummy ffrom unsplash -->
        <img
          :src="
            props.image ?? 'https://source.unsplash.com/1600x1500/?programming'
          "
          alt=""
          class="img-fluid rounded-5" />
      </div>
    </div>
  </div>
</template>
