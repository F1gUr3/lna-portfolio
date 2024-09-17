<script setup>
import { ref, onMounted } from "vue";

let { workName, shortDescription, image, longDescription } = defineProps({
  workName: String,
  shortDescription: String,
  image: String,
  longDescription: String,
});

const card = ref(null);

onMounted(() => {
  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add('pop');
          observer.disconnect();
        } 
      });
    },
    { threshold: 0.3}
  );

  if (card.value) {
    observer.observe(card.value);
  }
});
</script>

<template>
  <div ref="card" class="cardBody opacity-0 translate-y-10 transition-all duration-500 ease-out" :style="{ backgroundImage: `url(${image})` }">
    <div class="cardFilter"></div>
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

  box-shadow: 2px 2px 5px 1px #95959511, -2px -2px 5px 1px #ffffff0f;
  background-position: center;
  @apply m-auto bg-no-repeat relative rounded-xl;
}

.cardFilter {
  @apply absolute w-full h-full bg-[#00000030];
}

.cardText {
  h2 {
    @apply text-2xl font-semibold;
  }
  h3 {
    @apply font-thin;
  }
  @apply absolute bottom-0 left-0 p-4 w-full bg-[#191247d9] rounded-xl;
}

.pop {
  @apply opacity-100 translate-y-0;
}

</style>
