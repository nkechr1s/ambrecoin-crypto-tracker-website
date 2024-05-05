<template>
  <div class="feature-grid">
    <div v-for="(feature, index) in features" :key="index" class="feature">
      <img :src="feature.image" :alt="feature.title" class="feature-image" />
      <h3 class="feature-title">{{ feature.title }}</h3>
      <p class="feature-description">{{ feature.description }}</p>
    </div>
  </div>
</template>

<script>
import featureData from "../data/features.js";

export default {
  data() {
    return {
      features: featureData.features,
    };
  },
};
</script>

<style scoped>
.feature-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}

.feature {
  text-align: center;
}

.feature-image {
  width: 100%;
  height: auto;
  border-radius: 8px;
}

.feature-title {
  margin-top: 10px;
  font-size: 1.2rem;
}

.feature-description {
  margin-top: 5px;
  font-size: 1rem;
}
</style>
