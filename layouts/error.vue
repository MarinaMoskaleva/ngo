<template>
  <div class="error-block">
    <h1>О, нет! Ошибка :( Но не переживайте, у нас все под контролем!</h1>
    <h2>Статус ошибки: {{error.statusCode}}</h2>
    <h2>Сообщение: {{error.message}}</h2>
  </div>
</template>

<script>
  export default {
    props: {
      error: {
        type: Object,
        default: () => ({})
      }
    }

  }
</script>

<style scoped>
.error-block{
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  height: 100vh;
}

</style>
