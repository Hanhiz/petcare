<template>
  <div id="app">
    <Header />
    <HeroSection />
    <FeaturesSection />
    <ChooseUs />
    <TestimonialsSection />
    <PricingSection />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import HeroSection from './components/HeroSection.vue';
import FeaturesSection from './components/FeaturesSection.vue';
import ChooseUs from './components/ChooseUs.vue';
import PricingSection from './components/PricingSection.vue';
import TestimonialsSection from './components/TestimonialsSection.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    HeroSection,
    FeaturesSection,
    ChooseUs,
    TestimonialsSection,
    PricingSection,
    Footer,
  },
};
</script>

<style>
/* Global styles or CSS framework imports */
</style>
