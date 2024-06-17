<script>
export default {
   data() {
    return {
      valor1: null,
      valor2: null,
      nameSoft: "Calculadora de Luis Felipe Moquete",
      label1: "Valor 1",
      label2: "Valor 2" ,
      resultado: 0

    };
  },
  methods: {
    Postsumar() {
       this.resultado = parseInt(this.valor1) + parseInt(this.valor2);
    },
    Postrestar() {
       this.resultado = parseInt(this.valor1) - parseInt(this.valor2);
    },
    Postmultiplicar() {
       this.resultado = parseInt(this.valor1) * parseInt(this.valor2);
    },
    Postdividir() {
       this.resultado = parseInt(this.valor1) / parseInt(this.valor2);
    }, 
    
    }
    
  }
  
  

 
</script>

<template>
    <div>


<h2>{{ nameSoft }}</h2>
  <label>{{ label1 }}</label> <input type="text" v-model="valor1"  placeholder="Diga valor 1"/> <br>
  <label>{{ label2 }}</label> <input type="text"  v-model="valor2"   placeholder="Diga valor 2"/> <br>
  <button @click="Postsumar"> Sumar</button>
  <button @click="Postrestar"> Restar</button> <br>
  <button @click="Postmultiplicar"> Multiplicar</button>
  <button @click="Postdividir"> Dividir</button>

<br>
  <span v-if="valor1 > 0 && valor2 > 0">El resultado de la operación es: {{ resultado }}</span>
</div>


</template>

<style scoped>
 div { 
  background-color:rgb(89, 63, 63);
  color: white;
 }

</style>
