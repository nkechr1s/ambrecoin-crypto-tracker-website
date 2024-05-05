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
      <h1 v-if="title" class="hero-title">{{ title }}</h1>
      <p v-if="subTitle" class="left-p">{{ subTitle }}</p>

      <a
        target="_blank"
        rel="noreferrer"
        v-if="button"
        href="https://google.com"
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
  font-size: 32px;
  line-height: 55px;
  margin-top: 30px;
  max-width: 550px;
}

.left-p {
  line-height: 1.5;
  margin: 0 0 24px;
  color: #58667e;
  font-size: 16px;
  max-width: 580px;
  max-width: 460px;
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
</style>
