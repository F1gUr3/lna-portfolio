<script setup>
import {ref, onMounted} from 'vue';
import Step from "@/components/pageSubComponents/Step.vue";
import lightBulb from "@/components/icons/lightbulb.svg"
import development from "@/components/icons/development.svg"
import deliver from "@/components/icons/deliver.svg"
import RightArrow from "@/components/icons/rightArrow.svg"

let steps = ref(null)
onMounted(() => {
    const observer = new IntersectionObserver((entries) => {
        if(entries[0].isIntersecting){
            entries[0].target.classList.add("StepsPop")
            observer.disconnect();
        };

    },
    {threshold: 0.3}
);
    if(steps.value){
        observer.observe(steps.value);
    }
})


</script>

<template>
  <div class="Steps" ref="steps">
    <Step :image="lightBulb" name="Step one" description="Together we polish your ideas into executable designs, decide on what is the complete scope and start working on your aim." />
    <img :src="RightArrow" alt="Right Arrow">
    <Step :image="development" name="Step Two" description="Development begins. I create the first iterations of your project, keeping you updated on progress, while ensuring functionality and design remain top priorities." />
    <img :src="RightArrow" alt="Right Arrow">
    <Step :image="deliver" name="Step Three" description="We finalize the project, testing and fine-tuning the final product to ensure it meets all requirements before delivery." />
  </div>
</template>

<style scoped>
.Steps {
    @apply flex flex-row justify-center text-white -translate-x-16 opacity-0 duration-500
}
.StepsPop{
    @apply translate-x-0 opacity-100
}
</style>
