<script setup>
import {ref, onMounted} from 'vue';

let {typeOfSkill, percantage} = defineProps({
    typeOfSkill: String,
    percantage: Number,
})

let isVisible = ref(false);
let bar = ref(null);

onMounted(() => {
    const observer = new IntersectionObserver((entries) => {
        if(entries[0].isIntersecting){
            isVisible.value = true;
            observer.disconnect();
        }

    });
    if(bar.value){
            observer.observe(bar.value);
    };
});


</script>

<template>

<div class="barContainer" ref="bar">
<div class="textContainer">
<h3>{{ typeOfSkill }}</h3>  

<p id="percentage">{{ percantage }}%</p>
</div>
<div class="bar">
    <div class="percent" :style="{ width: isVisible ? percantage + '%' : '0%' }"></div>

</div>
</div>


</template>

<style scoped>
#percentage{
    @apply text-gray-400
}
.barContainer{
    @apply w-3/4 my-4
}
.textContainer{
    @apply flex flex-row justify-between w-full
}
.bar{
    @apply w-full rounded-xl bg-[#191247]  relative;
    height: 10px;
    .percent{
        @apply absolute bottom-0 left-0  bg-[#4700E8] rounded-xl;
        height: 10px;
        transition: width 1s ease;
        }
}

</style>