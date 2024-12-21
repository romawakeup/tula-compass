<script setup>
import CardList from './Cards/CardList.vue';

const cards = [
  { imgSrc: '/src/components/img/active.png', text: 'Активный отдых' },
  { imgSrc: '/src/components/img/museum.png', text: 'Музей' },
  { imgSrc: '/src/components/img/cafe.png', text: "Рестораны" },
  { imgSrc: '/src/components/img/park.png', text: "Парки" },
];
</script>

<template>
  <section class="what-places">
    <div class="container">
      <div class="what-places__wrapper">
        <h2 class="title-section">Какие места можно посетить?</h2>
        <CardList :cards="cards" />
      </div>
    </div>
  </section>
</template>



<style scoped>
.what-places {

}
</style>
