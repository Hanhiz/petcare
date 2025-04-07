<template>
  <section id="whyus" class="why-choose-us">
    <div class="container">
      <h2 class="section-title">Why Choose PetCare?</h2>
      <p class="section-subtitle">Your pet deserves the best. Here's why pet parents trust us:</p>

      <div class="circle-wrapper">
        <!-- Feature cards (no spinning now) -->
        <div class="rotating-ring">
          <div
            v-for="(feature, index) in features"
            :key="index"
            class="circle-card"
            :style="getPosition(index, features.length)"
          >
            <div class="icon">{{ feature.icon }}</div>
            <p>{{ feature.text }}</p>
          </div>
        </div>

        <!-- Center pet image -->
        <div class="center-circle">
          <img src="@/assets/image.png" alt="Cute Pet" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'WhyChooseUsSection',
  data() {
    return {
      features: [
        { icon: '🐾', text: 'Loving Caregivers' },
        { icon: '📆', text: 'Flexible Scheduling' },
        { icon: '🦴', text: 'Personalized Plans' },
        { icon: '🔒', text: 'Trust & Safety' },
        { icon: '📍', text: 'Real-Time Tracking' },
        { icon: '💬', text: '24/7 Support' }
      ]
    };
  },
  methods: {
    getPosition(index, total) {
      const radius = 250; // Circle radius
      const angle = (360 / total) * index;
      const x = 280 + radius * Math.cos((angle * Math.PI) / 180) - 60;
      const y = 285 + radius * Math.sin((angle * Math.PI) / 180) - 60;
      return {
        top: `${y}px`,
        left: `${x}px`
      };
    }
  }
};
</script>

<style scoped>
.why-choose-us {
  background-color: #F1F3F5; 
  padding: 5% 0;
  text-align: center;
  overflow: hidden;
}

.section-title {
  font-size: 2.2rem;
  font-weight: 700;
  color: #2f855a;
  margin-bottom: 0.5rem;
}

.section-subtitle {
  font-size: 1.1rem;
  color: #555;
}

.circle-wrapper {
  position: relative;
  width: 600px;
  height: 600px;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
}

.center-circle {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 250px; 
  height: 250px;
  transform: translate(-50%, -50%);
  border-radius: 50%;
  overflow: hidden;
  border: 8px solid #b2f2bb;
  box-shadow: 0 0 25px rgba(47, 133, 90, 0.3);
  z-index: 10;
  background: #fff;
}

.center-circle img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* Feature Cards */
.circle-card {
  position: absolute;
  width: 160px; 
  height: 160px; 
  background-color: #e6f4ea;
  border-radius: 50%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.08);
  transition: transform 0.3s ease;
  text-align: center;
  color: #2f855a;
  font-weight: 500;
  z-index: 1;
}

.circle-card:hover {
  transform: scale(1.08);
}

.icon {
  font-size: 2rem; 
}
</style>

