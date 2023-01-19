<script setup>
  import BreakingBadCardsSuspense from './components/BreakingBadCardsSuspense.vue';
  import RickAndMortyCards from './components/RickAndMortyCards.vue';
  import Hero from './components/Hero.vue';
  import { ref } from 'vue'

  const isBreakingBad = ref(true)
</script>

<template>
  <main>
    <Hero 
      :isBreakingBad="isBreakingBad" 
      @selectShow="isBreakingBad = !isBreakingBad"  
    />
    <BreakingBadCardsSuspense v-if="isBreakingBad" />
    <RickAndMortyCards v-else/>
  </main>
</template>


