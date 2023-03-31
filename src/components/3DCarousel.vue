<template>
  <div class="carousel-container-2">
    <div class="controls-2">
      <!-- <button class="circle-button left" @click="prevSlide">
        <div class="triangle left"></div>
      </button>
      <button class="circle-button right" @click="nextSlide">
        <div class="triangle right"></div>
      </button> -->
    </div>
    <div class="carousel-2">
      <div
        class="slides-2"
        :style="{ transform: `translateX(-${currentIndex * slideWidth}px)` }"
      >
        <div v-for="(story, index) in stories" :key="index" class="slide-2">
          <img :src="story.image" class="slide-image-2" />
        </div>
      </div>
    </div>
    <img class="blue-blob" src="../assets/icon/Blue-blob.svg">
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentIndex: 0,
      slideWidth: 460, // adjust this to match your slide width
      stories: [
        {
          image: require("@/assets/IMG_6129.jpg"),
        },
        {
        
          image: require("@/assets/IMG_6131.jpg"),
        },
        {
          image: require("@/assets/IMG_3268.jpg"),
        },
        {
          image: require("@/assets/IMG_6155.jpg"),
        },
      ],
    };
  },
  computed: {
    title() {
      return "Tentang cerita mereka";
    },
  },
  mounted() {
    setInterval(this.nextSlide, 5000); // call nextSlide method every 5 seconds
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
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  z-index: -100;
}
.carousel-2 {
  height: 306px;
  width: 450px;
  margin: 0 100px;
  overflow: hidden;
  border-radius: 10px;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
  position: relative;
}
.blue-blob {
  position: absolute;
  top: -10px;
  left: 120px;
  z-index: -1;
}
.slides-2 {
  width: 440px;
  display: flex;
  transition: transform 0.5s;
}

.slide-2 {
  width: 460px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.slide-image-2 {
  width: 460px;
  height: 306px;
  object-fit: cover;
  margin-right: 20px;
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
