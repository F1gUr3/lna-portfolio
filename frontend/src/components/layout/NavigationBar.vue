<script setup>
</script>

<template>

<div class="NavigationBar">
    <div id="logo">
        <p class="text-xl">Adrián Lukácsi</p>
    </div>    
    <div class="NavigationItems">
        <p>Home</p> 
        <p>Experience</p> <!--Replace with routerlinks-->
        <p>Contact</p>
    </div>
</div>

</template>

<style scoped>

.NavigationBar{
    @apply flex flex-row justify-between px-8 w-full p-4 my-auto bg-[#0C0537] text-white items-center;
    #logo p{
        @apply text-2xl ;
    }
    .NavigationItems{
        @apply flex flex-row gap-4 my-auto items-center; 
    }
    .NavigationItems p:last-child{
        @apply bg-[#8E85E8] text-[#0A0819] p-4 px-8 rounded-lg ;
    }
}
</style>