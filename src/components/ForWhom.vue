<script setup>
import CardList from './Cards/CardList.vue';

const cards = [
  { imgSrc: '/src/components/img/solo.png', text: 'Для одного человека' },
  { imgSrc: '/src/components/img/two.png', text: 'Для пары' },
  { imgSrc: '/src/components/img/family.png', text: "Для семьи" },
  { imgSrc: '/src/components/img/friends.png', text: "Для компании" },
];
</script>

<template>
  <section class="for-whom">
    <div class="container">
      <div class="for-whom__wrapper">
        <h2 class="title-section">Для кого Тульский компас?</h2>
        <CardList :cards="cards" />
      </div>
    </div>
  </section>
</template>



<style scoped>
.for-whom {



}


</style>
