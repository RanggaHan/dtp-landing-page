<template>
  <div class="impact-counter" ref="counterRef">
    <div class="background-image"></div>
    <div class="content-container">
      <h2>Uluran Tangan Kita</h2>
      <h1>OUR IMPACT 2023</h1>
      <div class="counter-container">
        <div class="counter-column">
          <div class="counter-box">
            <div>
              <img
                src="../assets/icon/earth.svg"
                alt="Logo 1"
                class="counter-logo"
              />
            </div>
            <div class="counter-text">
              <div class="counter-title">Ntraktir 7 Negara</div>
              <div class="counter">{{ beneficiaries[0] }}</div>
              <div class="counter-description">Penerima manfaat</div>
            </div>
          </div>
          <div class="counter-box">
            <div>
              <img
                src="../assets/icon/heart.svg"
                alt="Logo 2"
                class="counter-logo"
              />
            </div>
            <div class="counter-text">
              <div class="counter-title">Berbagi</div>
              <div class="counter">{{ beneficiaries[1] }}</div>
              <div class="counter-description">Penerima manfaat</div>
            </div>
          </div>
        </div>
        <div class="counter-column">
          <div class="counter-box">
            <div>
              <img
                src="../assets/icon/deal.svg"
                alt="Logo 3"
                class="counter-logo"
              />
            </div>
            <div class="counter-text">
              <div class="counter-title">Zakat Fitrah</div>
              <div class="counter">{{ beneficiaries[2] }}</div>
              <div class="counter-description">Penerima manfaat</div>
            </div>
          </div>
          <div class="counter-box">
            <div>
              <img
                src="../assets/icon/phone.svg"
                alt="Logo 4"
                class="counter-logo"
              />
            </div>
            <div class="counter-text">
              <div class="counter-title">Bantuan Sesama</div>
              <div class="counter">{{ beneficiaries[3] }}</div>
              <div class="counter-description">Penerima manfaat</div>
            </div>
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
      beneficiaries: [0, 0, 0, 0],
      targetBeneficiaries: [60094, 5000, 67000, 23000], // set your target numbers here
      duration: 5000, // set the duration of the animation here (in milliseconds)
      interval: null,
      counterActivated: false,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
    // this.startCounterAnimation();
  },
  unmounted() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      const counterEl = this.$refs.counterRef;
      const counterRect = counterEl.getBoundingClientRect();
      const windowHeight = window.innerHeight;
      const triggerBottom = windowHeight - windowHeight / 3; // change this value as per your requirement
      if (!this.counterActivated && counterRect.top < triggerBottom) {
        this.startCounterAnimation();
        this.counterActivated = true;
      }
    },
    startCounterAnimation() {
      let startTimestamp = null;
      let progress = 0;

      const step = (timestamp) => {
        if (!startTimestamp) startTimestamp = timestamp;
        progress = timestamp - startTimestamp;

        for (let i = 0; i < this.beneficiaries.length; i++) {
          const increment =
            (this.targetBeneficiaries[i] / this.duration) * progress;
          this.beneficiaries[i] = Math.min(
            Math.floor(increment),
            this.targetBeneficiaries[i]
          );
        }

        if (progress < this.duration) {
          window.requestAnimationFrame(step);
        }
      };

      this.interval = setInterval(() => {
        window.requestAnimationFrame(step);
        if (progress >= this.duration) {
          clearInterval(this.interval);
        }
      }, 1000);
    },
  },
};
</script>

<style>
.impact-counter {
  position: relative;
  margin-top: 175px;
  padding-bottom: 100px;
}
.background-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url("../assets/background/Counter-Background.png");
  background-size: cover;
  background-position: center;
  z-index: -1;
}
.content-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 50px;
}
.content-container h2 {
  color: #f5ad42;
  margin-top: 80px;
  margin-bottom: 0;
  font-size: 20px;
}
.content-container h1 {
  color: #ffffff;
  font-size: 35px;
}
.counter-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 50px;
  margin-top: 50px;
  margin-left: 40px;
  flex-direction: row;
  align-content: space-between;
  gap: 400px;
}
.counter-column {
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
  gap: 50px;
  align-content: flex-start;
  align-items: flex-start;
}
.counter-box {
  /* width: 300px;
  height: 300px; */
  margin: 20px;
  text-align: center;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.counter-logo {
  width: 80px;
  margin-bottom: 20px;
}
.counter-text {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  margin-left: 30px;
}
.counter-title {
  text-align: left;
  font-size: 25px;
  font-weight: 700;
  margin-bottom: 10px;
  color: #f5ad42;
}
.counter {
  font-size: 40px;
  font-weight: 500;
  margin-bottom: 10px;
  color: #ffffff;
}
.counter-description {
  font-size: 15px;
  font-weight: 700;
  color: #ffffff;
}
</style>
