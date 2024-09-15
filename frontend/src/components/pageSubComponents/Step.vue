<script setup>
let { image, name, description } = defineProps({
  image: String,
  name: String,
  description: String,
});
</script>

<template>
  <div class="stepContainer">
    <img :src="image" alt="An icon related to the step" />
    <p id="title">{{ name }}</p>
    <p id="description">{{ description }}</p>
  </div>
</template>

<style scoped>
.stepContainer {
  @apply w-96 h-96 flex justify-center items-center flex-col gap-8;
  img{
    @apply w-1/5
  }
  #title {
    @apply text-5xl font-thin;
  }
  #description{
    @apply font-thin text-center
  }
}
</style>
