<template>
  <div class="donation-images">
    <div class="text-container">
      <h2>
        Terhitung sejak 4 bulan terakhir, ratusan pengungsi Rohingya berlabuh di
        aceh, Indonesia.
      </h2>
      <p class="">
        Menjelang bulan ramadhan, mereka hidup serba terhimpit di camp
        pengungsian. Karenanya, bantuan yang turut kita salurkan, akan sangat
        berarti bagi mereka. Dalam bentuk makanan sahur dan berbuka, pakaian,
        air bersih dan lainnya. Jadikan bulan mulia sebagai kesempatan untuk
        menyemai amal sebanyak-banyaknya.
      </p>
      <button class="help-button">Donasi Sekarang</button>
    </div>
    <div class="images-container">
      <div class="image-column1">
        <img class="image-1" src="../assets/IMG_6064.jpg" alt="Cause 1" />
      </div>
      <div class="image-column2">
        <img class="image-2" src="../assets/IMG_3363.jpg" alt="Cause 2" />
        <img class="image-3" src="../assets/IMG_6073.jpg" alt="Cause 3" />
      </div>
    </div>
  </div>
</template>

<style>
.donation-images {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  padding: 50px;
  margin-left: 40px;
  margin-right: 40px;
  margin-top: 175px;
}

.text-container {
  width: 40%;
}

.text-container h2{
  font-size: 42px;
  width: 80%;
}

.text-container p{
  font-size: 26px;
  text-align: justify;
}

.help-button {
  margin-top: 10px;
  padding: 15px 26px;
  border: none;
  border-radius: 10px;
  background-color: #F5AD42;
  color: #ffffff;
  font-size: 16px;
  cursor: pointer;
}

.help-button:hover {
  background-color: #f4b75d;
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
}

.image-2 {
  width: 403px;
  height: auto;
  object-fit: cover;
  object-position: center;
  margin-bottom: 30px;
  border-radius: 20px;
}

.image-3 {
  width: 331px;
  height: auto;
  object-fit: cover;
  object-position: center;
  border-radius: 20px;
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
