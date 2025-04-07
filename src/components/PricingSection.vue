<template>
  <section id="pricing" class="py-16">
    <div class="pricing">
      <h2>Pricing Plans</h2>
      <div class="pp">
        <div
          class="p-t"
          v-for="(plan, index) in plans"
          :key="index"
        >
          <h3>{{ plan.name }}</h3>
          <p>{{ plan.description }}</p>
          <h2 class="p">{{ plan.price }}</h2>
          <button class="b-p">
            Choose plan
          </button>
          <br>
          <p class="m-d" v-on:click="toggleDetails(plan)">
            {{ plan.show ? 'Hide Details' : 'More details' }}
            <i :class="plan.show ? 'fa fa-angle-up' : 'fa fa-angle-down'"></i>
          </p>
          <ul v-if="plan.show" class="features-list">
            <li v-for="(feature, i) in plan.features" :key="i">
              {{ feature }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'PricingSection',
  data() {
    return {
      plans: [
        {
          name: 'Basic',
          description: 'Perfect for casual pet owners who just need occasional help.',
          price: '$49/month',
          features: [
            '🐶 2 Dog Walks / week',
            '🛁 1 Basic Grooming Session / month',
            '📆 Flexible Scheduling',
            '💬 Basic Support',
          ],
          show: false,
        },
        {
          name: 'Standard',
          description: 'Best for busy pet parents who want consistent care.',
          price: '$89/month',
          features: [
            '🐶 4 Dog Walks / week',
            '🛁 2 Full Grooming Sessions / month',
            '🐾 Pet Sitting (Up to 2 times / month)',
            '🐕‍🦺 Priority Booking',
          ],
          show: false,
        },
        {
          name: 'Premium',
          description: 'Full care for your furry friend with everything included.',
          price: '$149/month',
          features: [
            '🐶 Daily Dog Walks',
            '🛁 Unlimited Grooming Sessions',
            '🏡 Pet Sitting + Overnight Boarding (Up to 4 nights)',
            '🎁 Free Treat Box Every Month',
          ],
          show: false,
        },
      ],
    };
  },
  methods: {
    toggleDetails(plan) {
      plan.show = !plan.show;  // Toggle the show state for the clicked plan
    },
  },
};
</script>
<style scoped>
.pricing {
  color: rgb(25, 5, 67);
  margin-bottom: 50px;
}

h2 {
  font-size: 2.5rem;
  margin-bottom: 30px;
  color: #333;
  text-align: center;
}

.pp {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  gap: 20px;
  max-width: 1200px;
  margin: 0 auto;
}

.p-t {
  width: 28%;
  padding: 20px;
  height: auto;
  background: white;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  text-align: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.p-t:hover {
  background-color: rgb(241, 251, 252);
  transform: translateY(-5px);
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
}

.p {
  color: rgb(241, 45, 45);
  font-size: 1.5rem;
  font-weight: bold;
}

.b-p {
  background-color: rgb(45, 137, 168);
  color: white;
  padding: 10px 20px;
  font-size: 1.1rem;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease, transform 0.3s ease;
}

.b-p:hover {
  background-color: rgb(70, 178, 214);
  transform: scale(1.05);
}

.m-d {
  color: #328864;
  font-size: 1rem;
  cursor: pointer;
}

.m-d:hover {
  text-decoration: underline;
}

.features-list {
  list-style-type: none;
  padding: 0;
  margin-top: 10px;
  font-size: 1rem;
  color: #666;
}

.features-list li {
  margin-bottom: 5px;
}
</style>
