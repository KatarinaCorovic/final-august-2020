<template>
  <v-container fluid>
    <v-app class="cover">
        <v-row>
          <v-col cols="12" md="6">
            <div class="about">
              <h1>About us</h1>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ofprovident dignissimos qui? Sed vs qudantium aut.</p>
            </div>
          </v-col>
          <v-col cols="12" md="6">
            <div class="company">
              <h1>Company</h1>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ofprovident dignissimos qui? Sed vs qudantium aut.</p>
            </div>
          </v-col>

            <!-- //---------------    THREE DIVS -------------- -->

        
          </v-row>
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
                            <!-- <v-list-item-subtitle>by Kurt Wagner</v-list-item-subtitle> -->
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
                      <!-- <v-list-item-subtitle>by Kurt Wagner</v-list-item-subtitle> -->
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


   .cover{

        background-image: url(../assets/cargoship.jpg);
        min-height: 400px;
        background-size: cover;
        background-size: 100% 700px;
       //  background-position-y: -250px;
        background-repeat: no-repeat;
        position: relative;
        // opacity:0.5;
   }

   .about{
     width: 300px;
     height:300px;
     border-radius: 50%;
     background-color: white;
     transition:1s, width;
     margin-left:250px;
     margin-top:50px;
     

        h1{
          padding-top:30px;
          padding-left:80px;
        }

        p{
          padding:30px;
        }



   }

   .about:hover{
        transition:1s, width;
        width:700px;
        height:250px;
        border-radius:20px;
        // background-color:yellow;
        transition-duration:1s;
        // transition-delay:1s;
        transition-timing-function: linear;
       

   }

   .company{
      width: 300px;
     height:300px;
     border-radius: 50%;
     background-color: white;
     transition:1s, width;
     margin-top:330px;
    

      h1{
          padding-top:30px;
          padding-left:80px; 
        }

        p{
          padding:30px;
        }


   }

   .company:hover{
        transition:1s, width;
        width:700px;
        height:250px;
        border-radius:20px;
        // background-color:yellow;
        transition-duration:1s;
        // transition-delay:1s;
        transition-timing-function: linear;
       
   }

   .place{
         width: 300px;
         height:300px;
         border-radius: 50%;
         background-color: white;
         transition:1s, width;
         margin-left:300px;
         
         box-shadow: 2px 0px 2px 2px grey;

         h1{
          padding-top:30px;
          padding-left:50px;
        }

        p{
          padding:30px;
        }


   }


   .place:hover{
        transition:1s, width;
        width:500px;
        height:250px;
        border-radius:20px;
        // background-color:yellow;
        transition-duration:1s;
        // transition-delay:1s;
        transition-timing-function: linear;
       
   }

   .aboutDivs{

   .listOfPorts{
     margin-top:100px;
    

    }

    .efficiencyCard{
      margin-top:100px;
   
       

    }

       .howWeWork {
         margin-top:100px;
     

    }

   }


  @media only screen and (max-width:600px){
     .about{
         width:450px;
         height:500px;
         

     }
 }

   @media only screen and (max-width:600px){
     .company{
         width:450px;
         height:500px;

     }
 }
   
   

  
</style>