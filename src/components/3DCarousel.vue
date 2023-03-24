<template>
  <div class="carousel-container">
    <div class="carousel">
      <div class="carousel-inner" :style="carouselStyle">
        <div class="carousel-item" v-for="(item, index) in items" :key="index">
          <img :src="item.src" :alt="item.alt" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { src: "/assets/IMG_3363.jpg", alt: "Image 1" },
        { src: "/assets/IMG_3363.jpg", alt: "Image 2" },
        { src: "/assets/IMG_3363.jpg", alt: "Image 3" },
        { src: "/assets/IMG_3363.jpg", alt: "Image 4" },
        { src: "/assets/IMG_3363.jpg", alt: "Image 5" },
      ],
      selectedIndex: 0,
      animationInProgress: false,
    };
  },
  computed: {
    carouselStyle() {
      const angle = -90 * this.selectedIndex;
      const translateZ = -150 * this.selectedIndex;
      return {
        transform: `perspective(1000px) rotateX(${angle}deg) translateZ(${translateZ}px)`,
      };
    },
  },
  methods: {
    select(index) {
      if (this.animationInProgress) {
        return;
      }
      this.animationInProgress = true;
      setTimeout(() => {
        this.selectedIndex = index;
        this.animationInProgress = false;
      }, 1000);
    },
  },
};
</script>

<style>
.carousel-container {
  width: 100%;
  height: 300px;
  overflow: hidden;
}

.carousel {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  width: 100%;
}

.carousel-inner {
  display: flex;
  position: relative;
  transform-style: preserve-3d;
  transition: transform 1s;
}

.carousel-item {
  width: 200px;
  height: 200px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%) rotateY(0deg) translateZ(0);
  transition: transform 1s;
  opacity: 0.3;
}

.carousel-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.carousel-item.active {
  opacity: 1;
  transform: translate(-50%, -50%) rotateY(0deg) translateZ(0);
}

.carousel-item.active-1 {
  opacity: 0.8;
  transform: translate(-50%, -50%) rotateY(-20deg) translateZ(-150px);
}

.carousel-item.active-2 {
  opacity: 0.6;
  transform: translate(-50%, -50%) rotateY(-40deg) translateZ(-300px);
}

.carousel-item.active-3 {
  opacity: 0.4;
  transform: translate(-50%, -50%) rotateY(-60deg) translateZ(-450px);
}

.carousel-item.active-4 {
  opacity: 0.2;
  transform: translate(-50%, -50%) rotateY(-80deg) translateZ(-600px);
}
</style>
