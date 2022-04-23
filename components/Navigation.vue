<template>
    <nav class='navigation'>
        <Logo />
        <nuxt-link to='/'>Main</nuxt-link>
        <nuxt-link to='/about'>About page</nuxt-link>
        <nuxt-link to='/id'>ID page</nuxt-link>
        <nuxt-link to='/id/123'>ID 123</nuxt-link>
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
    }
</style>