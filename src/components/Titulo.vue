<template>
  <h1>{{texto}}</h1>
</template>

<script>
export default {
    name:'titulo',
    props:{
        texto : String
    }
}
</script>

<style scoped>
    h1 {
        font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
        color: rgb(122, 148, 148);
    }
</style>