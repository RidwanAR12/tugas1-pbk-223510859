<script setup>
import { ref } from "vue";
import Card from "../components/Card.vue";
import CardItem from "../components/CardItem.vue";
import List from "../components/ItemList.vue";

const skill = ref([
  "HTML",
  "CSS",
  "Javascript",
  "PHP",
  "SQL",
  "Python",
  "Vue",
]);

const education = ref([
  {
    year: "2022 - saat ini",
    major: "Bachelor of Informatic Enginering",
    location: "Islamic University of Riau",
    description:
      "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit fugiat quidem beatae modi eius possimus expedita, sint, eum perferendis dignissimos quas",
  },
  {
    year: "2016 - 2019",
    major: "Senior High School",
    location: "SMAIT Plus Bazma Brilliant Dumai",
    description:
      "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit fugiat quidem beatae modi eius possimus expedita, sint, eum perferendis dignissimos quas",
  },
  {
    year: "2013 - 2016",
    major: "Junior High School",
    location: "Ponpes Al-Ihsan Pekanbaru",
    description:
      "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit fugiat quidem beatae modi eius possimus expedita, sint, eum perferendis dignissimos quas",
  },
  {
    year: "2007 - 2013",
    major: "Elementary School",
    location: "SD 1 YKPP Dumai",
    description:
      "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit fugiat quidem beatae modi eius possimus expedita, sint, eum perferendis dignissimos quas",
  },
]);
</script>

<template>
  <!-- make resume component -->
  <div class="container" id="resume">
    <div class="col-md-6 mx-auto">
      <h1 class="text-center fw-bold fs-1">Resume</h1>

      <!-- Skill -->
      <h2 class="fw-bold mt-5">Skills</h2>
      <Card>
        <List :data="skill" />
      </Card>

      <!-- Experience -->
      <h2 class="fw-bold mt-5"></h2>
      <Card v-for="data in experience" class="mb-4">
        <CardItem
          :year="data.year"
          :job="data.job"
          :location="data.location"
          :description="data.description" />
      </Card>

      <!-- Education -->
      <h2 class="fw-bold mt-5">Education</h2>
      <Card v-for="data in education" class="mb-4">
        <CardItem
          yearColor="red"
          :year="data.year"
          :job="data.major"
          :location="data.location"
          :description="data.description" />
      </Card>
    </div>
  </div>

  
</template>

<style scoped>
#resume {
  margin-top: 100px;
  min-height: 100vh;
}

#experience .card,
#education .card {
  border: 0px;
}

#position {
  height: 150px;
  background-color: rgb(248, 248, 248);
  border-radius: 10px;
}

#position p {
  margin: 1px 0px;
}

#position #year {
  color: blue;
  font-weight: bold;
}

#position #location {
  font-size: 13px;
}
</style>
