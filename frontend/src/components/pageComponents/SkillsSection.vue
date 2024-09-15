<script setup>
import SkillBar from '@/components/pageSubComponents/SkillBar.vue';

let skills = [
    {
        name: "HTML+CSS+JS",
        percantage: 90,
    },
    {
        name: "Tailwind CSS",
        percantage: 80,
    },
    {
        name: "VueJS",
        percantage: 75,
    },
    {
        name: "Express JS",
        percantage: 40,
    },
    {
        name: "SQL",
        percantage: 90,
    },
    {
        name: "Python",
        percantage: 90,
    },
    {
        name: ".net C#",
        percantage: 80,
    },
    {
        name: "SEO",
        percantage: 80,
    },
]

</script>

<template>
<div class="SkillsContainer">
<SkillBar v-for="(item, index) in skills":typeOfSkill="item.name" :percantage="item.percantage" />

</div>
</template>

<style scoped>
.SkillsContainer{
    @apply grid grid-cols-2 m-auto justify-items-center items-center  text-white
}
</style>