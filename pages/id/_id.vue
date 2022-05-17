<template>
  <article class="container">
    <div class="block">
      <img class="image" src="https://i.pinimg.com/736x/84/90/4e/84904ef020fb4ddb32f057c623ee2e6f--dolly-parton.jpg" />
      <h1 class="title">Name of an artist</h1>
      <em class="subtitle">Country</em>
      <p>Description of an artist</p>
    </div>
  </article>
</template>

<script>
  export default {
    mounted(){
      console.log(this.$route, 'here is route');
    }

  }
</script>

<style scoped>
  .block {
    width: 40%;
    max-width: 400px;
    min-height: 650px;
    padding: 15px 30px;
    background: white;
    border-radius: 4px;
    text-align: left;
  }
  .image {
    width: 100%;
    height: 300px;
    object-fit: cover;
    object-position: left top;
  }
  .title {
    margin-bottom: 0;
  }
  .subtitle {
    display: block;
    margin-bottom: 15px;
  }
</style>
