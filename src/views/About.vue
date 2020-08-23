<template>
  <v-container fluid class="pa-0">
    <v-app>
      <div class="cover">
      <div class="aboutTitle">
        <h1>ABOUT US</h1>
      </div>
      </div>
   
            <!-- //---------------    THREE DIVS -------------- -->
        
      <v-row>
        <v-col cols="12" >
          <div class="aboutDivs">
            <v-row>
              <v-col cols="12" md="4">
                <v-card
                max-width="344"
                class="mx-auto listOfPorts"
                 >
                  <v-list-item>
                    <v-list-item-content>
                      <v-list-item-title class="headline">Our Headquarters</v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                  <v-img
                  src="../assets/map.jpg"
                  height="194"
                  ></v-img>
                  <v-card-title>List of ports:</v-card-title>
                  <v-spacer></v-spacer>
                  <v-card-actions>
                    <v-btn
                      icon
                      @click="show = !show"
                    >
                      <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
                    </v-btn>
                    </v-card-actions>
                      <v-expand-transition>
                        <div v-show="show">
                        <v-divider></v-divider>
                        <v-card-text>
                          <v-row>
                            <v-col cols="12" md="6">
                              <v-card-subtitle class="pb-0"><li>Bay of Algeciras</li></v-card-subtitle>
                              <v-card-subtitle class="pb-0"><li>Tarifa</li></v-card-subtitle>
                              <v-card-subtitle class="pb-0"><li>Almería</li></v-card-subtitle>
                              <v-card-subtitle class="pb-0"><li>Seville</li></v-card-subtitle>
                              <v-card-subtitle class="pb-0"><li>Málaga</li></v-card-subtitle>
                              <v-card-subtitle class="pb-0"><li>Ceuta</li></v-card-subtitle>
                            </v-col>
                            <v-col cols="12" md="6">
                              <v-card-subtitle class="pb-0"><li>Valencia</li></v-card-subtitle>
                              <v-card-subtitle class="pb-0"><li>Sagunto</li></v-card-subtitle>
                              <v-card-subtitle class="pb-0"><li>Gandía</li></v-card-subtitle>
                              <v-card-subtitle class="pb-0"><li>Melilla</li></v-card-subtitle>
                              <v-card-subtitle class="pb-0"><li>Barcelona</li></v-card-subtitle>
                              <v-card-subtitle class="pb-0"><li>Pasaia</li></v-card-subtitle>
                            </v-col>
                          </v-row>
                        </v-card-text>
                      </div>
                    </v-expand-transition>
                  <v-divider vertical></v-divider>
                </v-card>
              </v-col>

            <!---------------------- // SECOND DIV ------------------------->


              <v-col cols="12" md="4">
                <v-card
                  max-width="344"
                  class="mx-auto efficiencyCard"
                >
                  <v-list-item>
                    <v-list-item-content>
                      <v-list-item-title class="headline">Efficiency</v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                  <v-img
                    src="../assets/workers.jpg"
                    height="194"
                  ></v-img>
                  <v-card-title>How its done</v-card-title>
                  <v-card-text>
                  Lorem ipsum dolor sit, amet consectetur adipisicing elit. Esse cum, voluptate blanditiis odio, 
                  sapiente est.
                  </v-card-text>
                  <v-card-actions>
                    <v-btn
                      icon
                       @click="showPorts = !showPorts"
                      >
                      <v-icon>{{ showPorts ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
                    </v-btn>
                    </v-card-actions>
                      <v-expand-transition>
                        <div v-show="showPorts">
                        <v-divider></v-divider>
                        <v-card-text>
                          I'm a thing. But, like most politicians, he promised more than he could deliver. The bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.
                      </v-card-text>
                    </div>
                  </v-expand-transition>
                </v-card>
              </v-col>

                     
                 <!------------------ //THIRD DIV ------------------>


              <v-col cols="12" md="4">
                <v-card
                  max-width="344"
                  class="mx-auto howWeWork"
                  >
                  <v-list-item>
                    <v-list-item-content>
                      <v-list-item-title class="headline">Port import</v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                  <v-img
                        src="../assets/ourPort.jpg"
                        height="194"
                    ></v-img>
                    <v-card-title>Importing</v-card-title>
                      <v-card-text>
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit. 
                       Simos ea, voluptatum provident aperiam ipsa excepturi ab quam. 
                      </v-card-text>
                      <v-card-actions>
                       <v-btn
                        icon
                        @click="showBtn = !showBtn"
                      >
                  <v-icon>{{ showBtn ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
                </v-btn>
                </v-card-actions>
                <v-expand-transition>
                  <div v-show="showBtn">
                    <v-divider></v-divider>
                    <v-card-text>
                      I'm a thing. But, like most politicians, he promised more than he could deliver. The bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.
                    </v-card-text>
                    </div>
                  </v-expand-transition>
                </v-card>
              </v-col>
            </v-row>
          </div>
        </v-col>
      </v-row>
    </v-app>
  </v-container>
</template>

<script>
export default {
  name:'About',
   data: () => ({
      absolute: true,
      overlay: false,
      show: false,
      showBtn:false,
      showPorts:false,
      
    }),
}
</script>



<style scoped lang="scss">

.cover {
    background-image: url(../assets/cargoship.jpg);
    min-height: 550px;
    background-size: cover;
    background-position-y: -100px;
            
}

.aboutTitle {
    z-index:1;
    position: relative;
  
}

.aboutTitle h1 {
    padding-top:30px;
    color: rgb(233, 232, 219);
    font-weight: normal;
    font-size: 60px;
    text-align: center;
    z-index:2;

  }
    
h1 {
  text-align: center;
  padding-top:20px;
}

p {
  padding:30
}
  
.place {
    width: 300px;
    height:300px;
    border-radius: 50%;
    background-color: white;
    transition:1s, width;
     margin-left:300px;
    box-shadow: 2px 0px 2px 2px grey;

h1 {
  padding-top:30px;
  padding-left:50px;
  }

p {
  padding:30px;

}
}

  
  
</style>