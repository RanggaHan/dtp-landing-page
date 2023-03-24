<template>
  <div class="container">
    <div class="image-wrapper">
      <div class="gradient"></div>
      <img src="../assets/IMG_6529.jpg" alt="Image" />
    </div>
    <div class="text-wrapper-2">
      <p>
        "Aku ingin sekolah tinggi, menggapai mimpi-mimpi ku. Menjalankan shalat
        dan membaca Al Quran dengan aman, juga di akui sebagai warga negara di
        tempat yang berdaulat" tulis salah satu anak Rohingya dalam suratnya.
      </p>
      <div class="orange-line-2"></div>
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: row-reverse;
  align-items: center;
  justify-content: center;
  margin-top: 250px;
}
.image-wrapper {
  position: relative;
  width: 40%;
  height: 100%;
}

.image-wrapper img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.gradient {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    90deg,
    #fefeff 1.29%,
    #fefeff 1.3%,
    rgba(44, 61, 125, 0) 25%
  );
}

.text-wrapper-2 {
  width: 60%;
  padding: 2rem;
  text-align: left;
  margin-bottom: 100px;
}

.text-wrapper-2 p{
  font-weight: 600;
  font-size: 22px;
  line-height: 26.63px;
  color: #2C3D7D;
  margin-right: 120px;
  margin-left: 50px;
}

.orange-line-2 {
  content: "";
  margin-left: 50px;
  margin-top: 50px;
  bottom: 0;
  width: 60%;
  height: 5px;
  background-color: #F5AD42;
}
</style>
