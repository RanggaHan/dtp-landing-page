<template>
  <div class="impact-counter">
    <div class="background-image"></div>
    <div class="counter-container">
      <div class="counter">
        <img src="/path/to/logo1.png" alt="Logo 1" class="counter-logo" />
        <div class="counter-title">Counter 1 Title</div>
        <div class="counter-description">Counter 1 Description</div>
      </div>
      <div class="counter">
        <img src="/path/to/logo2.png" alt="Logo 2" class="counter-logo" />
        <div class="counter-title">Counter 2 Title</div>
        <div class="counter-description">Counter 2 Description</div>
      </div>
      <div class="counter">
        <img src="/path/to/logo3.png" alt="Logo 3" class="counter-logo" />
        <div class="counter-title">Counter 3 Title</div>
        <div class="counter-description">Counter 3 Description</div>
      </div>
      <div class="counter">
        <img src="/path/to/logo4.png" alt="Logo 4" class="counter-logo" />
        <div class="counter-title">Counter 4 Title</div>
        <div class="counter-description">Counter 4 Description</div>
      </div>
    </div>
  </div>
</template>

<style>
.impact-counter {
  position: relative;
  margin-top: 175px;
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
.counter-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  padding: 50px;
}
.counter {
  width: 300px;
  height: 300px;
  margin: 20px;
  background-color: #fff;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.counter-logo {
  width: 80px;
  margin-bottom: 20px;
}
.counter-title {
  font-size: 24px;
  font-weight: bold;
  margin-bottom: 10px;
}
.counter-description {
  font-size: 16px;
  color: #666;
}
</style>
