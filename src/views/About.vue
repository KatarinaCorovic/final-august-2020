<template>
  <v-app>
    <v-row>
      <v-col cols="12">
      <div class="cover"></div>
      </v-col>
    </v-row>
    <v-row justify="center">
        <v-btn
          color="success"
          class="mt-12"
          @click="overlay = !overlay"
        >
          Show Overlay
        </v-btn>

        <v-overlay
          :absolute="absolute"
          :value="overlay"
        >
       <v-card height="700" width="800" class="form">
         <v-btn
                icon
                @click="overlay = false"
              >
                <v-icon>mdi-close</v-icon>
              </v-btn>
             
              
          
            
          
          <!-- <v-form class="form">
                        <v-row>
                            <v-col cols=12 md="5">
                                <div class="input">
                                    <v-text-field outlined label="Ship name" autofocus="true"></v-text-field>
                                </div>
                            </v-col>
                        </v-row>
                        <v-row>
                            <v-col cols="12" md="5">
                                <div class="input">
                                    <v-text-field outlined label="Departure Port"></v-text-field>
                                </div>
                            </v-col>
                        
                            <v-col cols="12" md="5">
                                <div class="input">
                                    <v-text-field outlined label="Arrival Port" ></v-text-field>
                                </div>
                            </v-col>
                        </v-row>
                        <v-row>
                            <v-col cols="12" md="5">
                        <div class="input">
                            <v-text-field outlined label="Number of cargo"></v-text-field>  
                        </div>
                        </v-col>
                        <v-col cols="12" md="5">
                        <div class="input">
                            <v-text-field outlined label="Type of cargo" ></v-text-field>
                        </div>
                        </v-col>
                        </v-row>
                <v-row>
                     <v-col cols="12" md="5">
                        <div class="input">
                            <v-text-field outlined label="Departure Date" ></v-text-field>
                        </div>
                    </v-col>
                    <v-col cols="12" md="5">
                        <div class="input">
                            <v-text-field outlined label="Arrival Date" ></v-text-field>
                        </div>
                    </v-col>
                </v-row>
                <v-row>
                    <v-col cols="12" md="5" justify="center" align="center">
                        <v-btn>SUBMIT</v-btn>

                    </v-col>
                </v-row>

                    </v-form> -->
           
      </v-card>
        </v-overlay>
      </v-row>
 
  </v-app>
</template>


<script>
export default {
  name:'About',
   data: () => ({
      absolute: true,
      overlay: false,
    }),
}
</script>



<style scoped lang="scss">


   .cover{
     background-image: url(../assets/cargoship.jpg);
     min-height: 550px;
     background-size: cover;
     background-position-y: -350px;
     position: relative;
     opacity:0.3;
   }

   .form{
     background-color: red;
   }

</style>