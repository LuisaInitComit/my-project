<template>
  <div>
      <h1>Mi primer componente</h1>
      <!----Interpolación-->
      <h2>Calculadora</h2>
      <input type="number" id="num1" placeholder="numero_1" v-model="numero_1"/>
      <br />
      <br />
      <input type="number" ide="num2" placeholder="numero_2" v-model="numero_2"/>
      <br/>
      <button @click="sumar(numero_1, numero_2)">Sumar</button>
      <button @click="multiplicar(numero_1, numero_2)">Multiplicar</button>
      <button @click="dividir(numero_1, numero_2)">Dividir</button>
      <br />
      <br />
      <span id="resultado">Resultado: {{resultado}}</span>
  </div>
</template>

<script>
export default {
    //datos que manipulará el componente (variables "globales")
    data: ()=>{
        return{
            subtitulo: 'Calculadora',
            numero_1: null,
            numero_2: null,
            resultado: "",
        };
    },
    methods:{
        sumar(numero_1, numero_2){
            console.log("metodo sumar")
            console.log("Concatena: ", numero_1 + numero_2)
            //sumar valores
            this.resultado = parseInt(numero_1)+parseInt(numero_2)
        },
        multiplicar(){
            console.log("metodo multiplicar")
            console.log("Resultado: ", (numero_1, numero_2))
            //multiplicar valores
            this.resultado = parseFloat(this.numero_1)*parseFloat(this.numero_2)
        },
        dividir(){
            if(parseFloat(this.numero_2)==0){
                alert("No es posible realizar la división");
            } else{
                this.resultado= parseFloat(this.numero_1)/parseFloat(this.numero_2);
            }
        },
    },
    created: ()=>{
        console.log("Calculadora creada");
    },
};
</script>

<style>
</style>