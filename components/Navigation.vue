<template>
    <nav class='navigation'>
        <Logo :title="logoTitle"/>
        <nuxt-link
          v-for="item in routes"
          class='link'
          :to='item.path'
          :key='item.name'
        >
          {{item.name}}
        </nuxt-link>
        <button class='button' @click="toggleModal('Hello world', $event)">{{text}}</button>
        <Modal v-if='showModal' @closeModal='toggleModal'/>
    </nav>
</template>

<script>
    import Logo from './navigation/Logo'
    export default {
        components: {
            Logo
        },
        data() {
          return {
            text: 'Enter',
            logoTitle: 'НКО-проект',
            linkArray: [
              {to:'/', title:'Main'},
              {to:'/about', title:'About page'},
            ],
            showModal: false,
            counter: 0,
          }
        },
        methods: {
          toggleModal(data, event){
            console.log('data',data);
            console.log('event',event);
            this.showModal = !this.showModal;
          }
        },
        created(){
          if(this.$route.query.showModal){
            this.showModal = true;
          }
        },
        computed: {
          routes(){
            return this.$router.options.routes.filter(item => !item.path.includes((':')))
          }
        },
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
        background: rgba(255,255,255,0.2);
    }
    .button{
        width: 100px;
        background: white;
        padding: 10px 15px;
        color: black;
        border: 1px solid black;
        cursor: pointer;
        border-radius: 30px;
        transition: .3s;
    }
    .button:hover{
        background: black;
        color: white;
        transition: .3s;
    }
    .link{
        color: black;
    }
</style>
