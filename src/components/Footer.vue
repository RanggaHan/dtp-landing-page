<template>
  <footer class="footer">
    <div class="container">
      <div class="columns">
        <div class="column">
          <p class="copyright">&copy; DTPeduli 2023</p>
        </div>
        <div class="column">
          <h2>Kantor DT Peduli</h2>
          <div class="contact-container">
            <img src="../assets/icon/location.svg" alt="location" />
            <p class="address">
              Jl. Gegerkalong Girang No.32, Isola, Kec. Sukasari, Kota Bandung,
              Jawa Barat 40153
            </p>
          </div>
        </div>
        <div class="column">
          <h2>Kontak Kami</h2>
          <div class="contact-container">
            <img src="../assets/icon/phone.svg" alt="phone" />
            <p class="contact">021-123-456</p>
          </div>
        </div>
        <div class="column">
          <h2>Sosial Media</h2>
          <div class="social-media-container">
            <div class="social-media">
              <a href="facebook.com">
                <img src="../assets/logo/facebook-logo.svg" alt="facebook" />
              </a>
              <a href="twitter.com">
                <img src="../assets/logo/twitter-logo.svg" alt="twitter" />
              </a>
              <a href="youtube.com">
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
  </footer>
</template>

<script scoped>
export default {
  name: "BlueFooter",
};
</script>

<style>
.footer {
  background-color: #2c3d7d;
  color: #fff;
  padding: 30px 0;
  margin-top: 100px;
}

.container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  width: 100%;
}

.columns {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  width: 100%;
  margin-left: 50px;
}

.column {
  flex: 1;
  margin-right: 20px;
}

.column:last-child {
  margin-right: 0px;
}

.contact-container {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
}

.contact-container img {
  width: 20px;
  height: 20px;
  margin-right: 10px;
}

.social-media-container {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
}

.social-media {
  display: flex;
  flex-direction: column;
}

.social-media img {
  width: 30px;
  height: 30px;
  margin-right: 10px;
}

.social-media p {
  margin-top: 3px;
  margin-bottom: 13.5px;
}

a {
  color: #fff;
  margin-right: 10px;
}

img:hover {
  color: #ccc;
}
</style>
