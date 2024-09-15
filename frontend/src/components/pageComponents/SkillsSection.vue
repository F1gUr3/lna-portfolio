<script setup>
import SkillBar from '@/components/pageSubComponents/SkillBar.vue';

let skills = [
    {
        name: "HTML+CSS",
        percantage: 90,
    },
    {
        name: "HTML+CSS",
        percantage: 70,
    },
    {
        name: "HTML+CSS",
        percantage: 60,
    },
    {
        name: "HTML+CSS",
        percantage: 40,
    }
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