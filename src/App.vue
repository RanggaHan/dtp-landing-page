<template>
  <div>
    <HeaderCarousel></HeaderCarousel>
    <DonationImage1></DonationImage1>
    <ImpactCounter></ImpactCounter>
  </div>
</template>

<script>
import HeaderCarousel from './components/Carousel.vue';
import DonationImage1 from './components/DonationImage1.vue'
import ImpactCounter from './components/ImpactCounter.vue';

export default {
  name: 'App',
  components: {
    HeaderCarousel,
    DonationImage1,
    ImpactCounter,
  },
}
</script>

<style>
body {
  font-family: 'Poppins', sans-serif;
}
</style>
