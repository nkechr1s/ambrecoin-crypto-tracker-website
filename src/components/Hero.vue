<script setup>
defineProps({
  title: String,
  subTitle: String,
  button: Boolean,
});
</script>

<template>
  <div class="hero-area hero">
    <div class="left-col">
      <h1 v-if="title" class="hero-title" v-html="title"></h1>
      <p v-if="subTitle" class="left-p">{{ subTitle }}</p>

      <a
        target="_blank"
        rel="noreferrer"
        v-if="button"
        href="https://chromewebstore.google.com/detail/ambrecoin-crypto-prices/dpcmehikllndnhclamckhcnlhfokbakk"
      >
        <img class="download-btn" src="../assets/download.png"
      /></a>
    </div>
    <div class="right-col">
      <img src="../assets/hero-banner.png" />
    </div>
  </div>
</template>

<style scoped>
.hero-area {
  flex-direction: row;
  display: flex;
  justify-content: space-between;
  margin: 24px 0;
  align-items: center;
}

.hero-area.hero {
  height: 50vh;
  margin-bottom: 10rem;
  align-items: center;
}

.left-col h1 {
  font-weight: 700;
  font-size: 48px;
  line-height: 1.25;
  margin-top: 30px;
  max-width: 640px;
  background: -webkit-linear-gradient(315deg, #42d392 25%, #647eff);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-weight: 800;
  margin-bottom: 0px;
}

.left-p {
  background: linear-gradient(146deg, #fff, #757a7d);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  line-height: 1.5;
  transition: color 0.5s;
  font-size: 22px;
  max-width: 600px;
  font-weight: 500;
}

.right-col > img {
  object-fit: cover;
  max-width: 600px;
}

.download-btn {
  max-width: 220px;
  display: flex;
  justify-content: flex-start;
}

@media (max-width: 980px) {
  .hero-area {
    flex-direction: column;
    height: unset !important;
    margin-bottom: 5rem !important;
  }
  .left-col h1 {
    max-width: unset;
    font-size: 24px;
    margin-top: 5px;
    line-height: 125%;
  }
  .left-p {
    font-size: 14px;
  }
  .right-col > img {
    max-width: 300px;
  }
  .download-btn {
    max-width: 140px;
  }
}
</style>
