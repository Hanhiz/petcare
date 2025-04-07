<template>
  <section id="features">
    <div class="feature">
      <h2>Features</h2>
      <div class="features-container">
        <div class="feature-item">
          <img src="@/assets/dog-walking.gif" alt="Dog Walking" />
          <h3>Dog Walking</h3>
          <p>Daily walks to keep your dog active and happy.</p>
        </div>

        <div class="feature-item">
          <img src="@/assets/pet-sitting.png" alt="Pet Sitting" />
          <h3>Pet Sitting</h3>
          <p>Reliable care while you're away.</p>
        </div>

        <div class="feature-item">
          <img src="@/assets/7965936.png" alt="Pet Grooming" />
          <h3>Pet Grooming</h3>
          <p>Professional grooming to keep pets clean & healthy.</p>
        </div>

        <div class="feature-item">
          <img src="@/assets/1499532.png" alt="Pet Boarding" />
          <h3>Pet Boarding</h3>
          <p>Safe, comfy overnight stays.</p>
        </div>
      </div>

      <button class="explore-btn">Explore Our Services</button>
    </div>
  </section>
</template>
<script>
export default {
  name: 'FeaturesSection',
};
</script>
<style scoped>
#features {
  text-align: center;
  background-color: #FFFFFF;  /* White background for features */
  padding: 5% 0;
}

.features-container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  gap: 20px;
  max-width: 1200px;
  margin: 0 auto;
}

/* Feature Item Styling */
.feature-item {
  width: 21%;
  padding: 15px;
  height: 300px;
  background: white;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  text-align: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.feature-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);
}

/* Feature images */
.feature-item img {
  width: 120px;
  height: auto;
  margin-bottom: 10px;
  transition: transform 0.3s ease;
}

.feature-item:hover img {
  transform: scale(1.1);
}

h2 {
  font-size: 2.5rem;
  margin-bottom: 30px;
  color: #333;
}

h3 {
  font-size: 1.3rem;
  margin-bottom: 10px;
  color: #333;
}

p {
  color: #666;
  font-size: 1.1rem;
  line-height: 1.5;
}

/* Button Styling */
.explore-btn {
  margin-top: 30px;
  padding: 12px 20px;
  font-size: 1.2rem;
  background-color: #ff6b6b;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: 0.3s;
}

.explore-btn:hover {
  background-color: #ff4f4f;
  transform: scale(1.05);
}

</style>
