<template>
  <header>
    <img
      class="logo-header"
      alt="Logo - The Fit Club"
      src="@/assets/logo.png"
    />

    <ul class="menu-header">
      <li>Home</li>
      <li>Programs</li>
      <li>Why Us</li>
      <li>Plans</li>
      <li>Testimonials</li>
    </ul>
  </header>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: 'HeaderComponent'
})
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
}

.logo-header {
  height: 3rem;
  width: 10rem;
}

.menu-header {
  color: white;
  display: flex;
  gap: 2rem;
  list-style: none;
}

.menu-header > li:hover {
  color: var(--orange);
  cursor: pointer;
}
</style>