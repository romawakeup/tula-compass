<script setup>
import Card from './TheCard.vue';
defineProps(['cards']);
</script>

<template>
  <div class="cards__wrapper">
    <Card v-for="(card, index) in cards" :key="index" :imgSrc="card.imgSrc" :text="card.text" />
  </div>
</template>

<style scoped>
.cards__wrapper {
  display: flex;
  justify-content: space-between;
}
</style>
