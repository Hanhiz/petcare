<template>
  <section class="hero">
    <div class="hero-image"></div>
    <div class="hero-text">
      <h1>Keep Your Pets Happy with PetCare!</h1>
      <p>Trusted pet sitting, walking, and grooming services in your area.</p>
      <button>Book Now</button>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HeroSection',
};
</script>

<style scoped>
.hero {
  display: flex;
  position: relative;
  padding: 1%;
  height: 300px;
  border-radius: 5%;
  justify-content: center;
  align-items: center;
  background-color: white;
  overflow: hidden;
}

.hero-image {
  display: block;
  width: 100%;
  height: 100%;
  position: absolute;
  background-image: url("@/assets/hr-bg.avif");
  background-size: cover;
  background-position: center;
  filter: blur(3px);
}

.hero-text {
  z-index: 2;
  text-align: center;
  color: #4A4A4A;
}
</style>
