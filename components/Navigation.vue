<template>
    <nav class='navigation'>
        <Logo :title="logoTitle"/>
        <nuxt-link class='link' to='/'>Main</nuxt-link>
        <nuxt-link class='link' to='/about'>About page</nuxt-link>
        <button v-if="showBtn1" class='button'>{{text}}</button>
        <button v-else-if="showBtn2" class='button'>Я тест 1</button>
        <button v-else class='button'>А я тест 2</button>
        <Modal v-show='false'/>
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
            showBtn1: false,
            showBtn2: false,
          }
        }
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
