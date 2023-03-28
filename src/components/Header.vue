<template>
  <div class="header">
    <div class="logo-container">
      <img class="logo1" src="../assets/logo/dtp-logo.png" alt="Logo 1" />
      <img class="logo2" src="../assets/logo/unhcr-logo.svg" alt="Logo 2" />
    </div>
    <div class="button-container">
      <button class="button"><a href="https://dtpeduli.org/profil-lembaga" target="_blank">Tentang DT Peduli</a></button>
      <button class="button"><a href="https://www.unhcr.org/id/" target="_blank">Tentang UNHCR</a></button>
      <button class="donation-button"><a href="https://dtpeduli.org/ramadhan-bersama-rohingya" target="_blank">Donasi Sekarang</a></button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MainHeader',
}
</script>

<style>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  padding: 0px;
  z-index: 1;
  background-color: transparent;
}

.logo-container {
  display: flex;
  align-items: center;
  margin-left: 50px;
}

.logo1 {
  width: 160px;
  height: 100px;
  object-fit: cover;
}

.logo2 {
width: 160px;
  height: 100px;
  object-fit: cover;
}

.button-container {
  display: flex;
  align-items: center;
  margin-right: 60px;
}

.button {
  margin-left: 20px;
  padding: 10px 20px;
  border: none;
  border-radius: 20px;
  background-color: transparent;
  color: #ffffff;
  font-size: 14px;
  font-weight: 600;
  font-family: 'Poppins', sans-serif;
  cursor: pointer;
  transition: 0.3s; 
}

.button a {
  margin-right: 0;
}

.donation-button {
  margin-left: 20px;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  background-color: #E84F4F;
  color: #ffffff;
  font-size: 14px;
  font-weight: 600;
  font-family: 'Poppins', sans-serif;
  cursor: pointer;
  transition: 0.3s; 
}

.donation-button a {
  margin-right: 0;
}

.button:hover {
  background-color: #3e5baf;
  transition: 0.3s; 
}

.donation-button:hover {
  background-color: #e9a3a3;
  transition: 0.3s; 
}

a {
  text-decoration: none; /* remove underline */
  color: inherit; /* inherit the color from parent element */
}

</style>
