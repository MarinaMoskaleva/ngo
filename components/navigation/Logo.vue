<template>
    <h1>
        {{title}}
    </h1>
</template>

<script>
    export default {
        props: {
          title: {
            type: String,
            default: 'NGO'
          }
        }
    }
</script>

<style scoped>

</style>
