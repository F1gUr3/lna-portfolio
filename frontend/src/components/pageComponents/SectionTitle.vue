<script setup>

let {title, subTitle} = defineProps({
    title: String,
    subTitle: String
})

</script>

<template>

<div class="SectionTitle">
    <h2 class="title">{{ title }}</h2>
    <h3 class="subTitle">{{ subTitle }}</h3>

</div>
</template>

<style scoped>
.SectionTitle{
    @apply w-full text-center text-white mb-4;

    .title{
        @apply text-5xl font-light tracking-wider ;
    }
    .subTitle{
        @apply text-3xl font-thin text-[#8E85E8];

    }
}
</style>