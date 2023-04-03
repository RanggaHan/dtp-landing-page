<template>
  <div class="main-app-container">
    <HeaderCarousel></HeaderCarousel>
    <DonationImage1></DonationImage1>
    <ImpactCounter></ImpactCounter>
    <DonationImage2></DonationImage2>
    <ContentCarousel></ContentCarousel>
    <DonationImage3></DonationImage3>
    <OurPartners></OurPartners>
    <Footer></Footer>
  </div>
</template>

<script>
import HeaderCarousel from "./components/Carousel.vue";
import DonationImage1 from "./components/DonationImage1.vue";
import ImpactCounter from "./components/ImpactCounter.vue";
import DonationImage2 from "./components/DonationImage2.vue";
import ContentCarousel from "./components/ContentCarousel.vue";
import DonationImage3 from "./components/DonationImage3.vue";
import OurPartners from "./components/OurPartners.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    HeaderCarousel,
    DonationImage1,
    ImpactCounter,
    DonationImage2,
    ContentCarousel,
    DonationImage3,
    OurPartners,
    Footer,
  },
};
</script>

<style>
.main-app-container {
  display: flex;
  flex-wrap: nowrap;
  flex-direction: column;
  align-items: center;
  z-index: -2;
}
body {
  font-family: "Poppins", sans-serif;
}
</style>
