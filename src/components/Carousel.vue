<template>
  <div class="header-carousel">
    <Header></Header>
    <div class="slides" :style="{ transform: 'translateX(' + offset + 'px)' }">
      <div v-for="(image, index) in images" :key="index" class="slide">
        <img :src="image" alt="Slide {{index+1}}" />
      </div>
    </div>
    <div class="header-text-container">
      <div class="column1-header">
        <p class="header-text1">Ulur Tangan di Bulan</p>
        <p class="header-text2">Ramadhan</p>
      </div>
      <div class="column2-header">
        <p class="header-text3">
          Untuk Ratusan Etnis Muslim Rohingya, yang Bertahan Hidup di Camp
          Pengungsi
        </p>
      </div>
    </div>
    <div class="sequence-indicator">
      <div
        v-for="(image, index) in images"
        :key="index"
        class="dot"
        :class="{ active: index === currentIndex }"
        @click="goToSlide(index)"
      ></div>
    </div>
    <div class="controls">
      <button class="control prev" @click="prevSlide">
        <i class="fas fa-chevron-left"></i>
      </button>
      <button class="control next" @click="nextSlide">
        <i class="fas fa-chevron-right"></i>
      </button>
    </div>
  </div>
</template>

<script>
import Header from './Header.vue';

export default {
  name: "HeaderCarousel",
  components: {
    Header,
  },
  data() {
    return {
      images: [
        require("../assets/IMG_6165.jpg"),
        require("../assets/IMG_6857.jpg"),
        require("../assets/IMG_6212.jpg"),
      ],
      currentIndex: 0,
      offset: 0,
      slideWidth: 0,
    };
  },
  mounted() {
    this.slideWidth = this.$el.querySelector(".slide").offsetWidth;
    window.addEventListener("resize", this.handleResize);
  },
  beforeUnmount() {
    window.removeEventListener("resize", this.handleResize);
  },
  methods: {
    nextSlide() {
      this.currentIndex++;
      if (this.currentIndex >= this.images.length) {
        this.currentIndex = 0;
        this.offset = 0;
      } else {
        this.offset -= this.slideWidth;
      }
    },
    prevSlide() {
      this.currentIndex--;
      if (this.currentIndex < 0) {
        this.currentIndex = this.images.length - 1;
        this.offset = -this.slideWidth * (this.images.length - 1);
      } else {
        this.offset += this.slideWidth;
      }
    },
    goToSlide(index) {
      this.currentIndex = index;
      this.offset = -this.slideWidth * this.currentIndex;
    },
    handleResize() {
      this.slideWidth = this.$el.querySelector(".slide").offsetWidth;
      this.offset = -this.slideWidth * this.currentIndex;
    },
  },
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
}

.header-carousel {
  position: relative;
  overflow: hidden;
  width: 100%;
  height: 100%;
  z-index: 0;
}

.header-text-container {
  position: absolute;
  top: 62%;
  left: 50%;
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  align-items: center;
  transform: translate(-50%, -50%);
  z-index: 1;
}

.column1-header {
  margin-right: 40px;
  width: 150%;
}

.header-text1 {
  color: #ffffff;
  font-weight: 700;
  font-size: 48px;
  margin-bottom: 20px;
}

.header-text2 {
  color: #f5ad42;
  font-weight: 700;
  font-size: 48px;
  margin-top: 0;
}

.header-text3 {
  font-weight: 400;
  font-size: 28px;
  color: #ffffff;
  line-height: 1.5;
}

.slides {
  display: flex;
  transition: transform 0.5s ease-in-out;
}

.slide {
  flex: 0 0 auto;
  width: 100%;
  height: 100%;
  overflow: hidden;
}

.slide img {
  width: 100%;
  height: 980px;
  object-fit: cover;
  object-position: center;
}

.controls {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  display: flex;
  justify-content: space-between;
  width: 100%;
  padding: 0 20px;
}

.control {
  background: none;
  border: none;
  color: #ffffff;
  font-size: 48px;
  cursor: pointer;
  border-radius: 12px;
}

.prev {
  margin-right: 20px;
}

.next {
  margin-right: 40px;
}

.sequence-indicator {
  position: absolute;
  bottom: 10px;
  margin-bottom: 20px;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.dot {
  width: 20px;
  height: 20px;
  margin: 0 5px;
  border-radius: 50%;
  background-color: #f8f8f8;
  cursor: pointer;
}

.dot.active {
  background-color: #2c3d7d;
}
</style>
