<template>
  <footer>
    <div class="footer">
      <p>&copy; 2025 My Product, All rights reserved.</p>
      <div class="mt-4">
        <a href="#">&nbsp;Privacy Policy&nbsp;</a>
        <a href="#">&nbsp;Terms of Service&nbsp;</a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
};
</script>

<style scoped>
footer {
  align: center;
  background-color: #003366;
  color: white;
  padding: 2% 0;
}
footer a:hover {
  text-decoration: underline;
}
</style>
