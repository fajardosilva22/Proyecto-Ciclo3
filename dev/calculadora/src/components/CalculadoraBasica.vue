<template>
  <v-container>
      <v-row>
        <v-col>
          <h1 class="text-center">Calculadora Básica</h1>
        </v-col>
        
      </v-row>

      <v-row>
        <v-col>
          <v-text-field
            type="number"
            label="Numero 1"
            :rules="rules"
            hide-details="auto"
            v-model="n1"
            ></v-text-field>
        </v-col>  
        <v-col> 
          <v-text-field
            type="number"
            label="Número 2"
            :rules="rules"
            hide-details="auto"
            v-model="n2"
            ></v-text-field>
        </v-col> 

      </v-row>

      <!--<input type="number" v-model="n1"/>
      <input type="number" v-model="n2"/>-->
      <v-row class="text-center">
        <v-col>
            <v-btn
              color="secondary"
              elevation="20"
              rounded
              @click="suma()"
            >Sumar</v-btn>
        </v-col>
        <v-col>
            <v-btn
              color="primary"
              elevation="18"
              rounded
              @click="resta()"
            >Restar</v-btn> 
        </v-col>
        <v-col>
            <v-btn
              color="secondary"
              elevation="20"
              rounded
              @click="dividir()"
            >Dividir</v-btn>
        </v-col>
        <v-col>
            <v-btn
              
              color="primary"
              elevation="18"
              rounded
              @click="multiplicar()"
            >Multiplicar</v-btn> 
        </v-col>   
          <!--<button @click="suma()">Sumar</button>
          <button @click="resta()">Restar</button>-->
      </v-row>
      <br/>
      <span>{{ resultado }}</span>
  </v-container>
</template>

<script>
export default {
    name:"CalculadoraBasica",
    data:()=>{
        return{
            n1:null, 
            n2:null,
            resultado:"",
            rules: [
                 value => !!value || 'Requiredo.',
                 value => (value && value.length >= 2) || 'Minimo 1 caracteres',],
        }; 
    },
    methods:{
        suma(){
            this.resultado=parseFloat(this.n1) + parseFloat(this.n2);
        },
        resta(){
            this.resultado=parseFloat(this.n1) - parseFloat(this.n2);
        },
        dividir(){
          if(this.n2== 0){
              alert("Numero de la casilla 2, no es valido para dividir")
            }else{
              this.resultado=parseFloat(this.n1) / parseFloat(this.n2);
            }
            
        },
        multiplicar(){
            this.resultado=parseFloat(this.n1) * parseFloat(this.n2);
        },
    },
};
</script>

<style>

</style>