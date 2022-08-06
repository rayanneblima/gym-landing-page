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

    <div class="blur footer-blur-left"></div>
    <div class="blur footer-blur-right"></div>
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

.footer-blur-left {
  background: rgb(255, 115, 0);
  filter: blur(200px);

  bottom: 0;
  height: 12rem;
  left: 15%;
  width: 26rem;
}

.footer-blur-right {
  background: red;
  filter: blur(200px);

  bottom: 0;
  height: 12rem;
  right: 15%;
  width: 26rem;
}
</style>