<script setup>

let { title, isClicked } = defineProps({
  title: String,
  isClicked: Boolean
});

</script>

<template>
  <div :class="{filter: true, active: isClicked}" >
    <p>{{ title }}</p>
  </div>
</template>

<style scoped>

.filter{
        @apply flex justify-center p-4 m-4 text-[#8E85E8];
        border: 2px solid #8E85E8 ;
        border-radius: 5px;
    }
.active{
    @apply bg-[#8E85E8] text-black
}

</style>
