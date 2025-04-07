<template>
  <header class="header">
    <nav class="navbar">
      <!-- Logo Section -->
      <div class="logo">
        <img src="@/assets/logo.png" alt="Logo" class="logo-img" />
        <span class="logo-text">PetCare</span>
      </div>

      <!-- Navigation Links -->
      <ul class="nav-links">
        <li><a href="#features" class="nav-item">Features</a></li>
        <li><a href="#whyus" class="nav-item">Why Us</a></li>
        <li><a href="#pricing" class="nav-item">Pricing</a></li>
        <li><a href="#contact" class="nav-item">Contact</a></li>
      </ul>

      <!-- Mobile Menu Button -->
      <div class="mobile-menu" @click="toggleMenu">
        <span class="menu-icon"></span>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      isMenuOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    }
  }
};
</script>

<style scoped>
.header {
  background-color: #ffffff;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  padding: 0 30px;
  position: sticky;
  top: 0;
  z-index: 100;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
  flex-wrap: wrap;
}

/* Logo Section */
.logo {
  display: flex;
  align-items: center;
  gap: 10px;
}

.logo-img {
  width: 70px;
  height: auto;
}

.logo-text {
  font-size: 1.5rem;
  font-weight: 700;
  color: #002366;
  letter-spacing: 1px;
}

/* Navigation Links */
.nav-links {
  list-style: none;
  display: flex;
  gap: 30px;
}

.nav-item {
  text-decoration: none;
  color: #333;
  font-weight: 600;
  font-size: 1.1rem;
  transition: color 0.3s ease, transform 0.3s ease;
}

.nav-item:hover {
  color: #6BCB77;
  transform: translateY(-3px);
}

/* Mobile Menu Button */
.mobile-menu {
  display: none;
  cursor: pointer;
}

.menu-icon {
  width: 30px;
  height: 3px;
  background-color: #333;
  margin: 6px 0;
  transition: transform 0.3s ease;
}

</style>
