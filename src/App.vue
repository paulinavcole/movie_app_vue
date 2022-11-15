<script setup>
import { ref } from 'vue';
 import BreakingBadCardsVue from './components/BreakingBadCards.vue';
 import RickMortyCardsVue from './components/RickMortyCards.vue';

</script>

<template>
  <main>
    <h1>HERO</h1>
    <Suspense>
      <template #default>
        <BreakingBadCardsVue />
      </template>
      <template #fallback>
        <div>
          <p>Loading...</p>
        </div>
      </template>
    </Suspense>
    <RickMortyCardsVue />
   
  </main>
</template>