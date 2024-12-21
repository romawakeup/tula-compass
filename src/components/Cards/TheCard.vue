<script setup>
 defineProps(['imgSrc', 'text']);
</script>

<template>
  <div class="card">
    <div class="card__pic">
      <img :src="imgSrc" class="card__pic-img">
    </div>
      <p class="card__body-text">{{ text }}</p>
    <div class="card__body">
    </div>
  </div>
</template>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.card__pic {
  padding-bottom: 10px;
}

.card__pic-img {
  max-width: 100%;
  height: auto;
}

.card__body {}

.card__body-text {
  font-size: 1.3rem;
  font-weight: 500;
}

@media (max-width:768px) {
  .card__body-text {
  font-size: 1rem;

}
}

@media (max-width:500px) {
  .card__body-text {
  font-size: 0.7rem;

}
}
</style>
