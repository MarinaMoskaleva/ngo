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
  asyncData(){
    return axios.get("/guests").then(res => {
      const guests = res.data.data;
      return { guests }
    })
  }
};
</script>
