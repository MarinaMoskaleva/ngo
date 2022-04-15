<template>
  <div>
    <nav class='navigation'>
      <nuxt-link to='/'>Main</nuxt-link>
      <nuxt-link to='/about'>About page</nuxt-link>
      <nuxt-link to='/id'>ID page</nuxt-link>
      <nuxt-link to='/id/123'>ID 123</nuxt-link>
    </nav>
    <Nuxt />
  </div>
</template>

<script>
  export default {

  }
</script>

<style scoped>
  .navigation{
    width: 100%;
    height: 80px;
    padding: 20px;
    margin: 0;
    position: fixed;
    top: 0;
    left: 0;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: lightblue;
    box-sizing: border-box;
  }

</style>
