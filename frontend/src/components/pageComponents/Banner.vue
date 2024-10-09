<script setup>
import BannerImage from "@/assets/img/BannerImage.png";
</script>

<template>

  <div class="Banner">
    <div class="TextSection">
      <p id="BannerTitle">
        <span id="BannerTitleLight">Hey! I’m</span> <br />Adrián Lukácsi
      </p>
      <h1 id="BannerRole">Developer and designer</h1>

      <p id="contact">contact</p>
    </div>
    <div class="ImageSection">
      <img :src="BannerImage" alt="Image of myself" />
    </div>
  </div>
</template>

<style>
.Banner {
  @apply flex flex-row h-[600px] bg-[#0C0537] text-white;

  clip-path: polygon(100% 0%, 0% 0% , 0.00% 94.00%, 2.00% 93.96%, 4.00% 93.84%, 6.00% 93.64%, 8.00% 93.37%, 10.00% 93.04%, 12.00% 92.66%, 14.00% 92.25%, 16.00% 91.81%, 18.00% 91.37%, 20.00% 90.95%, 22.00% 90.54%, 24.00% 90.18%, 26.00% 89.87%, 28.00% 89.62%, 30.00% 89.45%, 32.00% 89.35%, 34.00% 89.34%, 36.00% 89.41%, 38.00% 89.56%, 40.00% 89.78%, 42.00% 90.07%, 44.00% 90.42%, 46.00% 90.81%, 48.00% 91.23%, 50.00% 91.67%, 52.00% 92.10%, 54.00% 92.53%, 56.00% 92.92%, 58.00% 93.26%, 60.00% 93.55%, 62.00% 93.78%, 64.00% 93.93%, 66.00% 94.00%, 68.00% 93.98%, 70.00% 93.89%, 72.00% 93.71%, 74.00% 93.46%, 76.00% 93.15%, 78.00% 92.79%, 80.00% 92.39%, 82.00% 91.96%, 84.00% 91.52%, 86.00% 91.09%, 88.00% 90.67%, 90.00% 90.30%, 92.00% 89.97%, 94.00% 89.70%, 96.00% 89.50%, 98.00% 89.37%, 100.00% 89.33%);  
  
  .TextSection {
    @apply m-auto items-center w-1/2 flex flex-col;
    #BannerTitle {
      @apply text-6xl md:text-8xl text-center font-bold relative m-4;
      background: -webkit-linear-gradient(120deg, #ffffff, #8a8a8a);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      #BannerTitleLight {
        @apply font-extralight;
        font-weight: thin !important;
      }
    }
    #BannerTitle::after{
        content: "";
        width: 100%;
        height: 5px;
        background: rgb(142,133,232);
        background: linear-gradient(90deg, rgba(142,133,232,1) 0%, rgba(71,0,232,1) 100%);
        position:absolute;
        bottom: 0;
        left: 0;
        border-radius: 5px
        
    }
    #BannerRole {
      @apply text-xl text-center font-light;
    }
    #contact {
      @apply p-4 bg-[#4700E8] text-center w-full md:w-1/2 m-8 text-3xl font-extralight rounded-lg;
    }
  }
  .ImageSection {
    @apply hidden md:flex  w-1/2   relative;
    img {
      @apply  h-full object-cover  ; 
    }
  }
}
</style>
