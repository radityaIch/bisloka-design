<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import Header from '@/components/Header.vue'
import HeroSection from '@/components/HeroSection.vue'
import CariBus from '@/components/CariBus.vue';
import FeatureSection from '@/components/FeatureSection.vue'
import BusListSection from '@/components/BusListSection.vue';
import FeedbackSection from '@/components/FeedbackSection.vue';
import Subscription from '@/components/Subscription.vue';
import Footer from '@/components/Footer.vue';
</script>

<template>
  <Header />
  <main>
    <HeroSection />
    <CariBus />
    <FeatureSection />
    <BusListSection />
    <FeedbackSection />
    <Subscription />
  </main>
  <Footer />
</template>

<script>
export default {
  name: 'App',
  components: {
    Header, HeroSection, CariBus, FeatureSection, BusListSection, FeedbackSection, Subscription, Footer
  }
}
</script>

<style>
  @font-face {
    font-family: "AmsiPro";
    src: local("AmsiPro"),
      url('@/assets/fonts/AmsiPro-Regular.otf') format("opentype");
  }
  @font-face {
    font-family: "AmsiProLight";
    src: local("AmsiPro"),
      url('@/assets/fonts/AmsiPro-Light.otf') format("opentype");
  }
  @font-face {
    font-family: "AmsiProSemiBold";
    src: local("AmsiPro"),
      url('@/assets/fonts/AmsiPro-Bold.otf') format("opentype");
  }
  @font-face {
    font-family: "AmsiProBold";
    src: local("AmsiPro"),
      url('@/assets/fonts/AmsiPro-SemiBold.otf') format("opentype");
  }
  @font-face {
    font-family: "AmsiProBlack";
    src: local("AmsiPro"),
      url('@/assets/fonts/AmsiPro-Black.otf') format("opentype");
  }
  @font-face {
    font-family: "GilroyBold";
    src: local("Gilroy"),
      url('@/assets/fonts/Gilroy-ExtraBold.otf') format("opentype");
  }
  @font-face {
    font-family: "GilroyLight";
    src: local("Gilroy"),
      url('@/assets/fonts/Gilroy-Light.otf') format("opentype");
  }
  *{
    font-family: "AmsiProLight";
    color: rgb(22, 22, 22);
  }
  @media (max-width: 1024px){
    body{
      overflow-x: hidden;
    }
  }
  .carousel__prev,
  .carousel__next {
    background-color:#fff;
    border: 5px solid #fff;
    border-radius: 100%;
    --tw-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
    --tw-shadow-colored: 0 10px 15px -3px var(--tw-shadow-color), 0 4px 6px -4px var(--tw-shadow-color);
    box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow);
    box-sizing: content-box;
    padding: 15px 15px 15px 15px;
  }
  .carousel__prev--in-active,
  .carousel__next--in-active {
    display: none;
  }
  .carousel__next{
    right: 1%;
  }
  .carousel__prev{
    left: 1%;
  }
  .carousel__icon{
    width: 2em;
    height: 2em;
    background-color:#fff;
    fill: #3BC5E9
  }
</style>