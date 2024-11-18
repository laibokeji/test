<script setup>
const features = [
  {
    title: '悠久历史',
    description: '始建于2000多年前，横跨中国北部的宏伟建筑'
  },
  {
    title: '文化象征',
    description: '中华文明的象征，世界文化遗产'
  },
  {
    title: '自然风光',
    description: '四季景色各异，山川秀丽，风景壮观'
  }
]
</script>

<template>
  <div class="great-wall">
    <header class="hero">
      <h1>长城旅游</h1>
      <p class="subtitle">探索世界奇迹，感受华夏文明</p>
    </header>

    <section class="features">
      <div v-for="(feature, index) in features" :key="index" class="feature-card">
        <h3>{{ feature.title }}</h3>
        <p>{{ feature.description }}</p>
      </div>
    </section>

    <section class="visit-info">
      <h2>参观信息</h2>
      <div class="info-grid">
        <div class="info-item">
          <h4>最佳时节</h4>
          <p>春秋两季，气候宜人</p>
        </div>
        <div class="info-item">
          <h4>著名景区</h4>
          <p>八达岭、慕田峪、金山岭</p>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
.great-wall {
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
}

.hero {
  text-align: center;
  padding: 4rem 0;
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
              url('https://images.unsplash.com/photo-1508804052814-cd3ba865a116?auto=format&fit=crop&w=1200&q=80') center/cover;
  color: white;
  border-radius: 8px;
  margin-bottom: 2rem;
}

.hero h1 {
  font-size: 3.5rem;
  margin-bottom: 1rem;
}

.subtitle {
  font-size: 1.5rem;
  opacity: 0.9;
}

.features {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  margin: 3rem 0;
}

.feature-card {
  padding: 2rem;
  background: #f8f8f8;
  border-radius: 8px;
  text-align: center;
  transition: transform 0.3s ease;
}

.feature-card:hover {
  transform: translateY(-5px);
}

.info-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.info-item {
  background: #fff;
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

h2, h3, h4 {
  color: #2c3e50;
}

@media (max-width: 768px) {
  .hero h1 {
    font-size: 2.5rem;
  }
  
  .subtitle {
    font-size: 1.2rem;
  }
}
</style>