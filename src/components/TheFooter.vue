<script setup>

</script>

<template>
  <footer class="footer">
    <div class="footer__wrapper">
      <h2 class="title-section title-section--footer">Присоединяйся к Тульскому компасу!</h2>
      <div class="btn-footer">
        <button class="btn-link"><a class="link" href="https://t.me/Visit_Tula_bot">Поехали!</a></button>
      </div>
    </div>
  </footer>
</template>

<style>
.footer {
  border-radius: 50px 50px 0 0;
  width: 100%;
  height: 300px;
  background-color: #FF2E50;
  display: flex;
  justify-content: center;
  align-items: center;
}

.footer__wrapper {

}

.title-section--footer {
  color: white;
}

.btn-footer {
justify-self: center;
}


@media (max-width:500px) {
  .footer {
  height: 150px;
}
}
</style>
