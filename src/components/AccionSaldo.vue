<template>
  <button @click="accion" :disabled="desactivar" >{{texto}}</button>
</template>

<script>
export default {
    name:'AccionSaldo',
    props:{
        texto : String,
        desactivar : {
            type : Boolean,
            default : false
        }
        
    },
    methods:{
        accion(){
            this.$emit('accion')
        }
    }
}
</script>

<style scoped>
    button{
        margin: 2px;
        padding: 10px;
        border-radius: 10px;
        outline-color: blue;
        cursor: pointer;

    }
    button:hover{
        background-color: cadetblue;
    }
</style>