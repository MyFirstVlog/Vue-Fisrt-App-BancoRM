<template>
<h2>Tipo de cuenta: {{cuenta}}</h2>
    <h3>Saldo:{{saldo}}</h3>
        <h4>Cuenta {{estado ? 'Activa' : 'Inactiva'}}</h4>
            <div v-for="(servicio , index) in servicios" :key="servicio">
                {{index + 1}}-{{ servicio }}
            </div>
                <AccionSaldo 
                    texto = 'Aumentar Saldo'
                    @accion = 'aumentar'
                />
                <AccionSaldo 
                    texto = 'Disminur Saldo'
                    @accion = 'disminuir'
                    :desactivar = 'desactivar'
                />
</template>

<script>
import AccionSaldo from './AccionSaldo.vue'


export default {
    name:'Cuenta',
    props: {

    },
    data() {
        return {
            saldo: 1000,
            cuenta: 'Visa',
            estado : true,
            servicios: ['transferencias', 'internacionales', 'consultas', 'bonos'],
            desactivar : false
        }
    },
    components:{
        AccionSaldo
    },
    methods:{
        aumentar(){
            this.saldo += 100 
            if(this.saldo > 0){
                this.desactivar = false
                return
            }
        },
        disminuir(){
            if(this.saldo === 0){
                this.desactivar = true 
                alert(`Saldo en ${this.saldo}`) 
                return
            }
            this.saldo -= 100 
        }
    }
}
</script>

<style>

</style>