<template>
  <v-container class="home">
    <v-row>
      <v-col class="text-center">
        <img  alt="Vue logo" src="../assets/logo.png">
        <Calculadora-basica/>
      </v-col>
    </v-row>
     <v-row>
      <v-col>
        <v-btn
          color="primary"
          elevation="18"
          rounded
          @click="paso1()">
        about</v-btn>
      </v-col>
    </v-row>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
    
   

    
    
  </v-container>
</template>

<script>
// @ is an alias to /src

import CalculadoraBasica from '../components/CalculadoraBasica.vue'

export default {
  name: 'Home',
  components: {
    CalculadoraBasica
  },
  methods: {
    paso1(){
      console.log("clic en boton about")
      this.$router.push("/about");
    }
  }
}
</script>
