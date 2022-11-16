<script setup>
 import BreakingBadCardsVue from './BreakingBadCards.vue';

</script>

<template>
<Suspense>
    <template #default>
      <BreakingBadCardsVue />
    </template>
    <template #fallback>
      <div class="cards spinner">
        <NSpin size="large" />
      </div>
    </template>
  </Suspense>

</template>

<style scoped>

.cards {
    max-width: 1000px;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    height: 700px
}
.cards h3 {
    font-weight: bold;
}
.cards p {
    font-size: 10px;
}
.jobs {
    display: flex;
    flex-wrap: wrap;
}
.button-container {
    display: flex;
    justify-content: center;
    padding-top: 30px
}
.button-container button {
    border: none;
    width: 50px;
    height: 50px;
    border-radius: 100%;
    margin: 0 5px;
    cursor: pointer;
}
.spinner {
    display: flex;
    align-items: center;
    justify-content: center;
}

p{
    font-size: 10px;
}
</style>