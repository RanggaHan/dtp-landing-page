<template>
  <div class="carousel-container-2">
    <div class="carousel-header-2">
      <h2>
        <span style="color: #2c3d7d">Tentang cerita</span>
        <span style="color: #f5ad42"> mereka</span>
      </h2>
      <div class="controls-2">
        <button class="circle-button left" @click="prevSlide">
          <div class="triangle left"></div>
        </button>
        <button class="circle-button right" @click="nextSlide">
          <div class="triangle right"></div>
        </button>
      </div>
    </div>
    <div class="carousel-2">
      <div
        class="slides-2"
        :style="{ transform: `translateX(-${currentIndex * slideWidth}px)` }"
      >
        <div v-for="(story, index) in stories" :key="index" class="slide-2">
          <img :src="story.image" class="slide-image-2" />
          <div class="slide-content-2">
            <p>{{ story.text1 }}</p>
            <p>{{ story.text2 }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentIndex: 0,
      slideWidth: 1278, // adjust this to match your slide width
      stories: [
        {
          text1:
            "Pada awal Maret 2023, DT Peduli bersama UNHCR sebagai Badan Pengungsi PBB, yang merupakan organisasi global untuk melindungi hak para pengungsi yang tidak berkewarganegaraan. Kami mengunjungi camp pengungsi yang ada di Sabang Indonesia, tepatnya daerah Pidie dan Aceh Besar. Puluhan anak-anak dengan senyum tulus mereka menyambut kami, jika manik matanya dapat bicara, mungkin dalam tatapan itu mereka sedang merintih meminta pertolongan.",
          text2:
            "Bagaimana tidak, mereka hidup ditempat penampungan yang belum layak sepenuhnya. Apalagi melihat kondisi ruang istirahat dan tempat menunaikan hajat. Belum ada tempat penampungan permanen yang dapat ditempati oleh para pengungsi. Namun sebelum itu, kita sama-sama mengusahakan untuk kebutuhan pokok seperti sandang, pangan, hygiene kits dan kebutuhan dasar lainnya.",
          image: require("@/assets/IMG_6633.jpg"),
        },
        {
          text1: "Sahabat, saudara-saudara kita, Muslim Rohingya yang saat ini terdampar di negeri kita, mereka menunggu uluran tangan kita. Begitu banyak memori kelam yang dialami anak-anak disana, mereka yang kehilangan orangtuanya, seorang istri yang sudah berstatus janda, kepala keluarga yang seorang diri sebab anak istri direnggut paksa darinya.",
          image: require("@/assets/IMG_6165.jpg"),
        },
        {
          text1: "Semoga bulan ramadhan tahun ini menggantikan seberkas memori kelam itu, dengan banyak keindahan yang merupakan buah dari kebaikan kita. Semoga ramadhan tahun ini kembali menyadarkan kita, bahwa barangkali dari segenap harta yang kita punya, ada hak oranglain dalam bagiannya.",
          image: require("@/assets/IMG_6857.jpg"),
        },
      ],
    };
  },
  computed: {
    title() {
      return "Tentang cerita mereka";
    },
  },
  methods: {
    prevSlide() {
      this.currentIndex =
        this.currentIndex === 0
          ? this.stories.length - 1
          : this.currentIndex - 1;
    },
    nextSlide() {
      this.currentIndex =
        this.currentIndex === this.stories.length - 1
          ? 0
          : this.currentIndex + 1;
    },
  },
};
</script>

<style scoped>
.carousel-container-2 {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 500px;
}

.carousel-header-2 {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  width: 1278px;
  margin-bottom: 20px;
  height: 100px;
}

.carousel-header-2 h2 {
  font-size: 40px;
  font-weight: 700;
}

.carousel-2 {
  height: 498px;
  width: 1278px;
  margin: 0 100px;
  overflow: hidden;
  border-radius: 10px;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
}

.slides-2 {
  width: 1278px;
  display: flex;
  transition: transform 0.5s;
}

.slide-2 {
  width: 1278px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.slide-image-2 {
  max-width: 486px;
  height: 498px;
  object-fit: cover;
  margin-right: 20px;
}

.slide-content-2 {
  flex: 1;
  width: 1278px;
}
.slide-content-2 p {
  text-align: justify;
  font-size: 18px;
  font-weight: 500;
  line-height: 21.78px;
  margin-right: 70px;
  margin-left: 60px;
}

.controls-2 {
  display: flex;
  justify-content: space-between;
  padding: 10px;
}
.circle-button {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background-color: #2c3d7d;
  border: none;
  cursor: pointer;
  margin-right: 10px;
}

.triangle {
  width: 0;
  height: 0;
  border-top: 10px solid transparent;
  border-bottom: 10px solid transparent;
  border-right: 10px solid white;
}

.left .triangle {
  transform: rotate(0deg) translateX(70%);
}

.right .triangle {
  transform: rotate(180deg) translateX(-100%);
}
</style>
