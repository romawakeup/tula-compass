<script setup>
import TheHeader from './components/TheHeader.vue';
import TheMain from './components/TheMain.vue';
import TheFooter from './components/TheFooter.vue';
import TheGarland from './components/TheGarland.vue';

const createSnowflake = () => {
  const snowflake = document.createElement('div');
  snowflake.className = 'snowflake';
  snowflake.innerHTML = '❄';
  snowflake.style.left = Math.random() * 100 + 'vw';
  snowflake.style.animationDuration = Math.random() * 3 + 2 + 's';
  snowflake.style.opacity = Math.random();
  snowflake.style.top = '-10px';
  document.body.appendChild(snowflake);

  snowflake.addEventListener('animationend', () => {
    snowflake.remove();
  });
};

setInterval(createSnowflake, 1000);
</script>

<template>
  <div class="#app">
    <TheGarland />
    <TheHeader />
    <TheMain class="indent"/>
    <TheFooter />
  </div>

</template>

<style>
.indent {
  margin: 150px 0 150px 0;
}

.container {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 20px;
}

.title-section {
  text-align: center;
  margin-bottom: 30px;
  font-size: 2rem;
  font-weight: 600;
}

.snowflake {
  position: absolute;
  top: -10px;
  color: rgb(148, 193, 211);
  font-size: 1rem;
  pointer-events: none;
  animation: fall linear infinite;
}

@keyframes fall {
  0% {
    transform: translateY(0);
  }

  100% {
    transform: translateY(calc(100vh + 1900px));
  }
}

.btn-link {
  padding: 15px 25px;
  border-radius: 10px;
  background-color: #240002;

}

.link {
  color: #fff1f3;
}

@media (max-width:768px) {
  .btn-link {
    padding: 7.5px 12.5px;
  }

  .title-section {
    font-size: 1.5rem;
  }

  .indent {
  margin: 100px 0 100px 0;
}
}

@media (max-width:500px) {
  .btn-link {
    padding: 5px 9px;
  }
  .title-section {
    font-size: 1rem;
  }

  .indent {
  margin: 50px 0 50px 0;
}
}
</style>
