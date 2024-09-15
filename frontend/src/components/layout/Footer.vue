<script setup>

</script>

<template>
<div class="w-full flex justify-center flex-col items-center   h-36 bg-[#0C0537] text-white" >
    <h3 class="font-bold">
        Adrián Lukácsi
    </h3>
    <p>All rights reserved ©2024 Adrián Lukácsi</p>
</div>

</template>

<style scoped>
h3{
    @apply relative text-3xl;
    z-index: 2;
}
h3::after{
    content: "";
    width: 100%;
    height: 15px;
    z-index: -1;
    @apply absolute bottom-0 left-0  bg-[#8d85e85d]
}


</style>