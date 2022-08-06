<template>
  <footer>
    <hr />

    <div class="footer-container">
      <div class="social-links">
        <img
          alt="Logo - Github"
          src="@/assets/github.png"
        />
        <img
          alt="Logo - Instagram"
          src="@/assets/instagram.png"
        />
        <img
          alt="Logo - Linkedin"
          src="@/assets/linkedin.png"
        />
      </div>

      <div class="logo-app">
        <img
          class="logo-footer"
          alt="Logo - The Fit Club"
          src="@/assets/logo.png"
        />
      </div>
    </div>
  </footer>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: 'FooterSection'
})
</script>

<style scoped>
footer {
  position: relative;
}

footer > hr {
  border: 1px solid var(--lightgray);
}

.footer-container {
  align-items: center;
  display: flex;
  flex-direction: column;
  gap: 4rem;
  height: 20rem;
  justify-content: center;
  padding: 1rem 2rem;
}

.social-links {
  display: flex;
  gap: 4rem;
}

.social-links > img {
  cursor: pointer;
  height: 2rem;
  width: 2rem;
}

.logo-app > img {
  width: 10rem;
}
</style>