<script setup>
import SectionTitle from "@/components/pageComponents/SectionTitle.vue"
</script>

<template>
  <div class="formBody">
    <SectionTitle title="Contact" subTitle="Feel free to reach out!" class="mt-4" />
    <form action="" class="contactForm">
      <input type="text" placeholder="Your Name" name="name" id="name" />
      <input type="email" placeholder="Your Email" name="email" id="email" />
      <input type="text" placeholder="Subject" name="subject" id="subject" />
      <textarea placeholder="Your Message" rows="6"></textarea>
      <button type="submit" class="submitButton">Send Message</button>
    </form>
  </div>
</template>

<style scoped>
.formBody {
  box-shadow: 2px 2px 15px 1px #95959505, -2px -2px 15px 1px #ffffff07;
  @apply m-auto w-1/2 h-auto bg-[#0F0B2A] rounded-xl mb-8 p-8;
}

.contactForm {
  @apply flex flex-col gap-8;
}

input, textarea {
  @apply w-full p-4 rounded-lg bg-[#1C1734] text-white border border-[#2B2845] focus:outline-none focus:ring-2 focus:ring-[#6A67D6] transition-all duration-300;
}

input::placeholder, textarea::placeholder {
  @apply text-[#8884B8];
}

textarea {
  @apply resize-none;
}

input:hover, textarea:hover {
  @apply bg-[#282249] border-[#6A67D6];
}

.submitButton {
  @apply bg-[#6A67D6] text-white font-semibold p-4 rounded-lg w-full cursor-pointer hover:bg-[#5A58B6] transition-all duration-300;
}

.submitButton:hover {
  @apply shadow-md shadow-[#6A67D6]/50;
}
</style>
