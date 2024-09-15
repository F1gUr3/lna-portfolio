<script setup>
import Layout from "@/components/layout/Layout.vue";
import Banner from "@/components/pageComponents/Banner.vue"
import SectionTitle from "@/components/pageComponents/SectionTitle.vue"
import PortfolioSection from "@/components/pageComponents/PortfolioSection.vue"
import SkillsSection from "@/components/pageComponents/SkillsSection.vue";

</script>

<template>

<Layout >

<Banner />
<SectionTitle title="About Me" subTitle="Who am I?" />
<div class="AboutMeText">
  <p>I am a young and enthusiastic Lorem Ipsum  Dolor Sit Amer Cons ecteteur  teteur   Dolor Sit A mer Consec ectetesec ecteteur  teteur   Dolor Sit A ur  teteur   Dolor Sit A  teteur   Dolor Sit A mer Con enthusiastic Lorem Ipsum  Dolor Sit Amer Cons ecteteur  teteur   Dolor Sit A mer Consec ectetesec</p>
</div>
<SectionTitle title="My Work" subTitle="What Do i Do?" />
<PortfolioSection />
<SectionTitle title="My Skills" subTitle="What am i good at?" />
<SkillsSection/>
<SectionTitle title="Work together" subTitle="How do we collaborate?" />
</Layout>

</template>

<style scoped>
.AboutMeText{
  @apply w-1/2 text-white m-auto text-center text-xl font-thin mb-4 tracking-wider;
  p{
    @apply my-16;
  }
}
</style>