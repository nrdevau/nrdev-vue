<script setup lang="ts">
const getImpactText = () => {
  return 'SURVIVE';
}
</script>
<template>
  <main>
    <div class="container mx-auto">
      <img class="profile" src="@/assets/profile.png">
      <div class="container mx-auto">
        <span>Helping you <span class="impact-text" v-text="getImpactText()"></span>online</span>
      </div>
      <img class="end-banner">
    </div>
    <h1>Assisting Startups, <a href="/scaleups">Scale-ups</a>, Brick and Mortar Businesses, Enterprise and even <a href="/agencies">Agencies</a></h1>
    <h2>We’ll help you wherever you are</h2>
    <h3 class="ribbon-bottom">How Can we Help?</h3>
    <ActionList />
    <h3 class="ribbon-bottom">Our Happy Clients</h3>
    <TestimonialList />
  </main>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
