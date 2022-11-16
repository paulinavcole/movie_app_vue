<script setup>
 import { ref } from 'vue';
 import BreakingBadCardsSuspenseVue from './components/BreakingBadCardsSuspense.vue';
 import RickMortyCardsVue from './components/RickMortyCards.vue';
 import HeroVue from './components/Hero.vue';

const isBreakingBad = ref(true);
</script>

<template>
  <main>
    <HeroVue 
    :isBreakingBad="isBreakingBad"
    @selectShow="isBreakingBad = !isBreakingBad"
  />
  
  <KeepAlive>
    <Component :is="isBreakingBad ? BreakingBadCardsSuspenseVue : RickMortyCardsVue"  />
  </KeepAlive>
  </main>
</template>

<style scoped>
.cards{
  height: 700px;
  background-color: rgb(27, 26, 26);
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>