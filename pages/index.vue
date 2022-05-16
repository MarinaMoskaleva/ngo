<template>
  <div class="container">
    <UserCard v-for="guest in guests" :guest="guest" :key="guest.attributes.slug"/>
  </div>
</template>

<script>
import axios from '@/plugins/axios'

export default {
  data() {
  return {
    guests: []
  }
  },
  created() {
    axios.get("/api/guests").then(res => {
      this.guests = res.data.data;
      console.log(res.data.data)
    })
  }
};
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
