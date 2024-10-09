<script setup>
import { ref } from 'vue';

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
</script>

<template>
  <div class="NavigationBar">
    <div id="logo">
      <p class="text-xl">Adrián Lukácsi</p>
    </div>    
    <div class="NavigationItems">
      <div class="hamburger" @click="toggleMenu">
        <div class="slice"></div>
        <div class="slice"></div>
        <div class="slice"></div>
      </div>
      <div :class="{ 'open': isMenuOpen }" class="menu">
        <p>Home</p>
        <p>Experience</p>
        <p>Contact</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.NavigationBar {
  @apply flex flex-row justify-between px-8 w-full p-4 my-auto bg-[#0C0537] text-white items-center;
}

#logo p {
  @apply text-2xl relative text-[#dbdae3];
  z-index: 20;
}

#logo p::after {
  content: "";
  width: 100%;
  height: 15px;
  z-index: -1;
  @apply absolute bottom-0 left-0 bg-[#8d85e85d];
}

.NavigationItems {
  @apply flex-row gap-4 my-auto items-center;
}

.hamburger {
  @apply flex flex-col gap-1 cursor-pointer md:hidden;
}

.slice {
  @apply h-1 w-6 bg-white rounded-full;
}

.menu {
  @apply flex-row gap-4 my-auto items-center hidden md:flex relative;

}

.menu p {
  @apply text-white;
}

.menu p:last-child {
  @apply bg-[#8E85E8] text-[#0A0819] p-4 px-8 rounded-lg;
}

.menu.open {
    backdrop-filter: blur(12px);
    opacity: 1;

    animation: appear 0.3s forwards;

  @apply flex flex-col absolute left-1/2 -translate-x-1/2 z-10 m-auto bg-[#0c053751] h-96 justify-center items-center w-full ;
}


@keyframes appear{
    from{
        display: none;
        opacity: 0;
    }
    to{
        display: flex;
        opacity: 1;
    }
}

</style>
