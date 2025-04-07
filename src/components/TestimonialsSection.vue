<template>
  <section class="testimonials">
    <div class="container">
      <h2 class="section-title">What Our Clients Say</h2>
      <p class="section-subtitle">Hear from our happy pet parents!</p>

      <!-- Testimonial Cards -->
      <div class="testimonials-wrapper">
        <div
          v-for="(testimonial, index) in testimonials"
          :key="index"
          class="testimonial-card"
        >
          <div class="client-info">
            <img :src="testimonial.photo" alt="Client Photo" class="client-photo" />
            <div class="client-details">
              <p class="client-name">{{ testimonial.name }}</p>
              <div class="client-rating">
                <span v-for="star in 5" :key="star" class="star">&#9733;</span>
              </div>
            </div>
          </div>
          <p class="testimonial-text">"{{ testimonial.text }}"</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
// Import images
import client1 from '@/assets/client1.png';
import client2 from '@/assets/client2.png';
import client3 from '@/assets/client3.png';

export default {
  name: 'TestimonialsSection',
  data() {
    return {
      testimonials: [
        {
          name: 'John Doe',
          photo: client2,
          text: 'PetCare has been amazing for our dog! They are so caring and attentive!',
        },
        {
          name: 'Jane Smith',
          photo: client1,
          text: 'I can always trust PetCare to take care of my cat when I am away.',
        },
        {
          name: 'Paul White',
          photo: client3,
          text: 'The team at PetCare provides excellent service with love and passion!',
        }
      ]
    };
  }
};
</script>

<style scoped>
.testimonials {
  padding: 4rem 1rem;
  background-color: #f9fafb;
  text-align: center;
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
  margin-bottom: 2rem;
}

.testimonials-wrapper {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 2rem;
}

.testimonial-card {
  background-color: #ffffff;
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
  text-align: left;
}

.testimonial-card:hover {
  transform: translateY(-10px);
}

.client-info {
  display: flex;
  align-items: center;
  margin-bottom: 1rem;
}

.client-photo {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  object-fit: cover;
  margin-right: 1rem;
}

.client-details {
  text-align: left;
}

.client-name {
  font-weight: bold;
  color: #2f855a;
  margin-bottom: 0.3rem;
}

.client-rating .star {
  color: #f59e0b;
  font-size: 1rem;
}

.testimonial-text {
  font-size: 1rem;
  color: #333;
  line-height: 1.5;
  font-style: italic;
}
</style>
