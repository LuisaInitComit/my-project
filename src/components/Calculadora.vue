<template>
  <div>
      <h1>Mi primer componente</h1>
      <!----Interpolación-->
      <h2>Calculadora</h2>
      <input type="number" id="num1" placeholder="numero_1"/>
      <br>
      <input type="number" ide="num2" placeholder="numero_2"/>
      <br>
      <!---<button @click="">Sumar</button>-->
  </div>
</template>

<script>
export default {
    //datos que manipulará el componente (variables "globales")
    data: ()=>{
        return{
            subtitulo: 'Calculadora',
            numero_1: null,
            numero_2: null
        }
    },
    methods:{
        sumar(){
            console.log("metodo sumer")
            console.log("Resultado: ", (numero_1, numero_2))
        }
    },
    created: ()=>{
        console.log("Calculadora creada")
    }

}
</script>

<style>

</style>