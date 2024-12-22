<script setup>

</script>

<template>
  <header class="header">
    <div class="container">
      <div class="header__wrapper">
        <div class="logo">
          <p class="logo__text">Тульский компас</p>
          <img src="./icons/logo.svg" class="logo__icon" >
        </div>
        <button class="btn-link"><a class="link" href="https://t.me/Visit_Tula_bot">Перейти к боту</a></button>
      </div>

    </div>
  </header>
</template>

<style scoped>
.header {
padding-top: 50px;
}

.header__wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;

}

.logo {
  display: flex;
  align-items: center;
  gap: 1rem;
  font-weight: 600;
}

.logo__icon{
max-width: 45px;
}

.logo__text {
  font-size: 2.5rem;
}

@media (max-width:768px) {
  .logo__text {
  font-size: 2rem;
}
.logo__icon{
max-width: 35px;
}

.logo{
  gap: 0.7rem;
}
}

@media (max-width:500px) {
  .logo__text {
  font-size: 1.2rem;
}
.logo__icon{
max-width: 25px;
}
.logo{
  gap: 0.5rem;
}}

</style>
