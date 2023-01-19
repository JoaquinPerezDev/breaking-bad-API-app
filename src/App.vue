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
    <!-- The below code is an alternative to using the Component component 
    <BreakingBadCardsSuspense v-if="isBreakingBad" />
    <RickAndMortyCards v-else/>
    -->
    <KeepAlive>
      <Component :is="isBreakingBad ? BreakingBadCardsSuspense : RickAndMortyCards"  />
    </KeepAlive>
  </main>
</template>


