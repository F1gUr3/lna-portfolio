<script setup>
import { ref } from "vue";

import PortfolioFilter from "@/components/pageSubComponents/PortfolioFilter.vue";

let filters = ["Web development", "UI/UX design", "Project Management"];
let clickedIndex = ref(0);

function handleClick(index) {
  clickedIndex.value = index;
}

let isClicked = ref();

</script>

<template>
  <div class="filters">
    <PortfolioFilter
      class="filter"
      v-for="(item, index) in filters"
      :key="index"
      @click="handleClick(index)"
      :isClicked="clickedIndex === index"
      :title="item"
    />
  </div>
</template>

<style scoped>
.filters {
  @apply flex flex-row justify-center items-center;
}
</style>
