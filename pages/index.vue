<template>
  <div class="main-page">
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
  .main-page{
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>