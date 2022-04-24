<template>
    <nav class='navigation'>
        <Logo />
        <nuxt-link class='link' to='/'>Main</nuxt-link>
        <nuxt-link class='link' to='/about'>About page</nuxt-link>
        <button class='button'>Enter</button>
        <!--<Modal />-->
    </nav>
</template>

<script>
    import Logo from './navigation/Logo'
    export default {
        components: {
            Logo
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