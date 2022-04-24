<template>
  <div class="container">
  <Test />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage'
})

</script>

<style scoped>
  .container{
    background: url('~/static/background.jpg') center no-repeat;
    height: 100vh;
    background-size: cover;
    margin: 0 auto;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
</style>