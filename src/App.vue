<script setup>
  import BreakingBadCards from './components/BreakingBadCards.vue';
  import RickAndMortyCards from './components/RickAndMortyCards.vue';
  import PracticeSlot from './components/PracticeSlot.vue';
</script>

<template>
  <main>
    <h1>HERO</h1>
    <Suspense>
      <template #default>
        <BreakingBadCards  />
      </template>
      <template #fallback>
        <div>
          <p>Loading...</p>
        </div>
      </template>
    </Suspense>
    <RickAndMortyCards />
    <PracticeSlot>

    </PracticeSlot>
  </main>
</template>

