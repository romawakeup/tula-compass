<script setup>
import { ref } from 'vue';

const questionsData = ref([
  { question: 'Как начать пользоваться Тульским компасом?', answer: 'Чтобы начать использовать Тульский компас, запустите бота в Telegram. Вы можете сделать это, нажав на кнопку перехода, расположенную в шапке и подвале нашего сайта. Следуйте простым инструкциям: выберите время, количество человек, место и тип отдыха. На основе ваших предпочтений Тульский компас подберет идеальные места для прогулок!' },
  { question: 'Как предлагается маршрут?', answer: 'Маршрут предлагается в зависимости от вашего времени, компании и желаемого вида отдыха.' },
  { question: 'Как рассчитывается время на маршрут?', answer: 'Время на маршрут рассчитывается с использованием формулы Хаверсина для определения расстояния между двумя точками на карте, которое затем делится на среднюю скорость передвижения по Туле — 20 км/ч.' },
  { question: 'Могу ли я добавить свой маршрут?', answer: 'Да, вы можете добавить свое место, отправив описание этого места боту в Telegram.' },
  { question: 'Какие функции есть в телеграм-боте Тульский компас?', answer: 'Бот предлагает множество функций, включая генерацию разнообразных маршрутов, выбор отдельных туристических мест, возможность добавления их в избранное, прогноз погоды и добавление собственных маршрутов.' },
  { question: 'Какие перспективы развития Тульского компаса?', answer: 'В планах на будущее — добавление функции "Достижения"' },
]);

const openIndex = ref(null);

const toggle = (index) => {
  openIndex.value = openIndex.value === index ? null : index;
};

const isOpen = (index) => {
  return openIndex.value === index;
};
</script>

<template>
  <section class="answers-questions">
    <div class="container">
      <div class="answers-questions__wrapper">
        <h2 class="title-section">Ответы на вопросы</h2>
        <div v-for="(item, index) in questionsData" :key="index" class="accordion-item">
          <div class="accordion-title" @click="toggle(index)">
            <span>{{ item.question }}</span>
            <span class="toggle-icon">{{ isOpen(index) ? '-' : '+' }}</span>
          </div>
          <div v-if="isOpen(index)" class="accordion-content">
            <p>{{ item.answer }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.answers-questions {

}

.accordion-item {
  border-radius: 10px;
  overflow: hidden;
  margin-bottom: 10px;
}

.accordion-title {
  padding: 15px;
  background-color: #FF2E50;
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #fff;
  font-weight: 400;
  font-size: 1.3rem;
}

.accordion-content {
  padding: 10px;
  background-color: #fff;
}

@media (max-width:768px) {
  .accordion-title {
  padding: 15px;
  font-size: 1rem;
}
}

@media (max-width:500px) {
  .accordion-title {
  padding: 10px;
  font-size: 0.7rem;
}
}
</style>
