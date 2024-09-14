<script setup>
import { defineProps } from "vue";

let { workName, shortDescription, image, longDescription } = defineProps({
  workName: String,
  shortDescription: String,
  image: String,
  longDescription: String,
});
</script>

<template>
  <div class="cardBody" :style="{ backgroundImage: `url(${image})` }">
    <div class="cardFilter">

    </div>
    <div class="cardText">
        <h2>{{ workName }}</h2>
        <h3>{{ shortDescription }}</h3>
    </div>
  </div>
</template>

<style scoped>
* {
  @apply text-white;
}

.cardBody {
  width: 400px;
  height: 500px;
  background-size: cover;

  box-shadow:  2px 2px 5px 1px #95959511,
  -2px -2px 5px 1px #ffffff0f;
  background-position: center;
  @apply m-auto bg-no-repeat relative rounded-xl;
  .cardFilter{
    
    @apply absolute w-full h-full bg-[#00000030] 
  }
  .cardText{
    h2{
        @apply text-2xl font-semibold
    }
    h3{
        @apply font-thin
    }
    @apply absolute bottom-0 left-0 p-4 w-full bg-[#191247d9] rounded-xl
  }
}

</style>
