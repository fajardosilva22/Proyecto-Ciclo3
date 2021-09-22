<template>
  <v-app >
    <v-toolbar color="purple" dark  id="nav"  flex-grow= 0>
          <v-toolbar-title>
            <img  alt="Vue logo" src="@/assets/logo.png">
          </v-toolbar-title>

          <v-divider class="mx-4" vertical> 
          </v-divider>

          <span class="subheading">My Home</span>

          <v-spacer></v-spacer>

          <v-toolbar-items class="hidden-sm-and-down">
            <v-btn  to="/" text>
              Calculadora
            </v-btn>

            <v-divider vertical></v-divider>

            <v-btn text to="/personajescards">
              Cards Personajes
            </v-btn>

            <v-divider vertical></v-divider>

            <v-btn text to="/about">
              About
            </v-btn>
            <v-divider vertical></v-divider>
          </v-toolbar-items>
          
      </v-toolbar>
      <v-container>
        <router-view/>
      </v-container>
      
  </v-app>
  
</template>
<!--<div id="app"> ejemplo de link
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>-->
<style>

</style>
