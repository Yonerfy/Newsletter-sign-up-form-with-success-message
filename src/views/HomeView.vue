<script setup>
import NewsletterCard from '../components/NewsletterCard.vue'
</script>

<template>
  <div class="home">
    <main>
      <NewsletterCard />
    </main>
  </div>
</template>

<style scoped>
  .home {
    background-color: #fff;
    border-radius: 2em;
    padding: 2em;
    display: flex;
    justify-content: space-around;
  }
  @media (max-width: 768px) {
    .home {
      height: initial;
      display: initial;
      width: 100%;
    }
  }
</style>
