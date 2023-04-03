<template>
  <footer class="footer">
    <div class="container">
      <div class="columns">
        <div class="column">
          <p class="copyright">&copy; DTPeduli 2023</p>
        </div>
        <div class="right-text-container">
          <div class="address-container">
          <h2>Kantor DT Peduli</h2>
          <div class="address">
            <img src="../assets/icon/location.svg" alt="location" />
            <p>
              Jl. Gegerkalong Girang No.32, Isola, Kec. Sukasari, Kota Bandung,
              Jawa Barat 40153
            </p>
          </div>
        </div>
        <div class="contact-container">
          <h2>Kontak Kami</h2>
          <div class="number-container">
            <img src="../assets/icon/phone.svg" alt="phone" />
            <p class="contact">021-123-456</p>
          </div>
        </div>
        <div class="social-media-container">
          <h2>Sosial Media</h2>
          <div class="social-media-logo-container">
            <div class="social-media">
              <a href="https://web.facebook.com/lazdtpeduli/?_rdc=1&_rdr" target="_blank">
                <img src="../assets/logo/facebook-logo.svg" alt="facebook" />
              </a>
              <a href="https://twitter.com/dtpeduli?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor" target="_blank">
                <img src="../assets/logo/twitter-logo.svg" alt="twitter" />
              </a>
              <a href="https://www.youtube.com/@DTPeduli/about" target="_blank">
                <img src="../assets/logo/youtube-logo.svg" alt="youtube" />
              </a>
            </div>
            <div class="social-media">
              <p>Facebook</p>
              <p>Twitter</p>
              <p>Youtube</p>
            </div>
          </div>
        </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script scoped>
export default {
  name: "BlueFooter",
};
</script>

<style scoped>
.footer {
  background-color: #2c3d7d;
  color: #fff;
  width: 100%;
  height: 100%;
  padding-top: 50px;
  padding-bottom: 80px;
  margin-top: 100px;
}

.container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  width: 100%;
}

.right-text-container {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  align-items: flex-start;
}

.columns {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  width: 100%;
  margin-left: 50px;
  margin-right: 50px;
}

.column {
  flex: 1;
  margin-right: 20px;
}

.address-container {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
  margin-left: 20px;
}

.address-container h2 {
  font-size: 14px;
  font-weight: 700;
  line-height: 17.5px;
}

.contact-container {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
  margin-left: 70px;
  margin-right: -50px;
}

.social-media-container {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
  margin-left: 20px;
}

.number-container {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
}

.address {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
}

.address img {
  width: 27px;
  height: 27px;
}

.number-container img {
  width: 20px;
  height: 20px;
  margin-right: 10px;
}

.social-media-logo-container {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
}

.social-media {
  display: flex;
  flex-direction: column;
}

.social-media img {
  width: 27px;
  height: 27px;
}

.social-media p {
  font-weight: 600;
  margin-top: 5.5px;
  margin-bottom: 13.5px;
}

h2 {
  font-size: 15px;
  font-weight: 800;
  line-height: 18.15px;
}

p {
  width: 180px;
  margin-left: 10px;
  font-weight: 400;
  font-size: 10px;
  line-height: 12.1px;
}

a {
  color: #fff;
  margin-right: 10px;
}

img:hover {
  color: #ccc;
}
</style>
