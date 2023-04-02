<template>
  <div class="donation-images">
    <div class="images-container">
      <Carousel></Carousel>
      <div class="text-container">
        <h2>
          Setelah terombang-ambing, takdir melabuhkan perahu mereka di pesisir
          pantai Indonesia
        </h2>
        <p>
          "Setelah 21 hari berlayar kami berlabuh di sini, tapi kami tidak tahu
          nama negara ini. Setelah fajar, masyarakat setempat mulai membantu
          kami. Mereka memberi kami tempat dan tidak menolak kami. Kami sangat
          berterima kasih dan bersyukur kepada masyarakat Indonesia." Ungkapan
          salah satu pengungsi Rohingya, Ummi Kalsum.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import Carousel from './3DCarousel.vue';
export default {
  name: 'DonationImage2',
  components: {
    Carousel,
  },
};
</script>

<style scoped>
.donation-images {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  width: 1278px;
  margin-top: 175px;
}

.text-container {
  margin-left: 175px;
}

.text-container h2 {
  font-size: 30px;
  line-height: 45px;
  font-weight: 600;
  width: 100%;
  color: #2c3d7d;
}

.text-container p {
  font-weight: 500;
  font-size: 20px;
  line-height: 24.2px;
  text-align: justify;
  width: 90%;
  margin-top: 40px;
}

.images-container {
  display: flex;
  flex-direction: row;
  align-items: center;
}

.image-column2 {
  display: flex;
  flex-direction: column;
  margin-left: 30px;
}

.image-1 {
  width: 221px;
  height: auto;
  object-fit: cover;
  object-position: center;
  border-radius: 20px;
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
}

.image-2 {
  width: 403px;
  height: auto;
  object-fit: cover;
  object-position: center;
  margin-bottom: 30px;
  border-radius: 20px;
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
}

.image-3 {
  width: 331px;
  height: auto;
  object-fit: cover;
  object-position: center;
  border-radius: 20px;
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
}

.donation-images__image {
  margin-bottom: 30px;
}

.donation-images__image img {
  width: 100%;
}

.donation-images__image h3 {
  margin-top: 20px;
}

.donation-images__image p {
  margin-top: 10px;
}
</style>
