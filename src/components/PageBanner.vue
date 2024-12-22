<script setup>

</script>

<template>
  <section class="page-banner">
    <div class="container">
      <div class="page-banner__wrapper">
        <div class="page-banner__description">
          <h1 class="page-banner__title">Тульский компас - Ваш путеводитель по идеальному выходному дню!</h1>
          <p class="page-banner__text">Отправляйтесь в увлекательное приключение с Тульским компасом - Вашим надежным
            партнером для
            организации идеального выходного дня.</p>
          <p class="page-banner__text">Наши готовые маршруты помогут вам открыть новые места, насладиться красотой
            природы, попробовать
            вкусные блюда и создать незабываемые воспоминания.</p>
          <p class="page-banner__text">Планируйте свой идеальный выходной с Тульским компасом!</p>
        </div>
        <img src="./icons/bubble.png" class="page-banner__img">
      </div>
    </div>
  </section>
</template>

<style scoped>
.page-banner {}

.page-banner__wrapper {
  display: flex;
  justify-content: space-between;
}

.page-banner__description {
  max-width: 700px;
}

.page-banner__title {
  margin-bottom: 30px;
  font-size: 2rem;
  font-weight: 600;

}

.page-banner__text {
  margin-bottom: 15px;
  font-size: 1.5rem;
}

.page-banner__img{

}

@media (max-width:960px) {
  .page-banner__img{
    display: none;
  }
}

@media (max-width:768px) {
  .page-banner__title {
    font-size: 1.2rem;
  }

  .page-banner__text {

    font-size: 1rem;
  }
}

@media (max-width:500px) {
  .page-banner__title {
    font-size: 0.9rem;
    margin-bottom: 15px;
  }

  .page-banner__text {
    font-size: 0.8rem;
  }

  .page-banner__img{
    max-width: 50%;
    max-height: 10%;
  }
}
</style>
