<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import FooterView from './views/FooterView.vue'

const callToAction = () => {
  console.log('calling to action');
}

</script>

<template>
  <header>
    <RouterLink to="/"><img alt="NRDev logo" class="logo" src="@/assets/nrdev-logo.svg" width="125px"/></RouterLink>
    <nav>
      <RouterLink to="/services">Services</RouterLink>
      <RouterLink to="/blog">Blog</RouterLink>
      <button v-on:click="callToAction()">Get in touch</button>
    </nav>
  </header>

  <RouterView />
  <FooterView />
</template>

<style scoped>
header {
  display: block;
  line-height: 1.5;
  max-height: 100vh;
  width: 100%;
  background-color: #2BA48D;
}

.logo {
  display: block;
  margin: 0 auto;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
