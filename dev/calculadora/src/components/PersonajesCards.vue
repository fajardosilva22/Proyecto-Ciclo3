<template>
  <div>
      <h1 class="text-center">Personajes</h1>
        <v-row>
            <v-col v-for="item in personajes" :key="item.Name">
            
                <v-col>
                <v-card class="mx-auto" max-width="344">
                    <v-img :src="item.PicUrl" alt="Cargando imagen..." height=200px
                      display: flex
                      flex-flow: column wrap >
                        
                        
                    </v-img>
                    <v-card-title>
                        {{item.Name}}
                    </v-card-title>
                    <v-card-subtitle>
                        <v-row>
                            <v-col>
                                 Species : {{item.Species}}
                            </v-col>
                            <v-col>
                                Age : {{item.Age}}
                            </v-col>
                        </v-row>
                    </v-card-subtitle>

                    <v-card-actions>
                        <v-btn color="orange lighten-2" text>
                            Explore
                        </v-btn>

                        <v-spacer></v-spacer>

                        <v-btn icon @click="show = !show">
                            <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
                        </v-btn>
                    </v-card-actions>

                    <v-expand-transition>
                        <div v-show="show">
                            <v-divider></v-divider>

                            <v-card-text>
                                <v-row>
                                    <v-col>
                                        Planet = "{{item.Planet}}"
                                    </v-col>
                                    <v-col>
                                        Status = {{item.Status}}
                                    </v-col>
                                </v-row>
                                <v-row>
                                    <v-col>
                                    Profession = {{item.Profession}} <br>
                                    FirstAppearance = "{{item.FirstAppearance}}" <br>
                                    Relatives = {{item.Relatives}} <br>
                                    "VoicedBy" = {{item.VoicedBy}} <br>
                                    </v-col>
                                    
                                    
                                </v-row>
                               
                            
                            </v-card-text>
                        
                        </div>
                    </v-expand-transition>
                </v-card>
                </v-col>
                
                <br>
            </v-col>
        </v-row>
  </div>

</template>
<script>
import store from "../store/index.js";

export default {
    data: () => ({
        show: false, 
        
    }),
    methods:{  
        
    },
    created: () => {
        //accede a las acciones del store
        store.dispatch("getPersonajes");
    },
    computed:{
        personajes: () => {
            return store.state.personajes;
        }
    }

}
</script>
