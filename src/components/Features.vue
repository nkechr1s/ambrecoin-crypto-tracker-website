<template>
  <div class="feature-grid">
    <div v-for="(feature, index) in features" :key="index" class="feature">
      <img
        v-if="feature.image"
        :src="feature.image"
        :alt="feature.title"
        class="feature-image"
      />
      <h2 v-if="feature.title" class="feature-title">{{ feature.title }}</h2>
      <p v-if="feature.description" class="feature-description">
        {{ feature.description }}
      </p>
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
  max-width: 60px;
}

.feature-title {
  margin-top: 10px;
  font-size: 1.2rem;
}

.feature-description {
  margin-top: 5px;
  font-size: 1rem;
}

@media (max-width: 980px) {
  .feature-grid {
    display: grid;
    grid-template-columns: repeat(1, 1fr);
    gap: 20px;
  }
  .feature-image{
    max-width:40px;
  }
  .feature {
  text-align: left;
 }
 .feature-description{
    font-size:14px;
 }
}
</style>
