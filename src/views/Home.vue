<template>
  <v-container fluid>
    <v-app>
      <v-row>
       <v-col cols="12">
          <div class="cover">
            <v-btn depressed color="#ffb32a" class="button">PLACE THE ORDER</v-btn>
          </div>
            <i class="fas fa-ship"></i>
      
            <div class="picture" >
      
              <v-btn fab color="#0a3158"><v-icon>mdi-domain</v-icon></v-btn>
              <v-btn fab color="#0a3158"><v-icon>mdi-vuetify</v-icon></v-btn> 
              <v-btn fab color="#0a3158"><v-icon>mdi-heart</v-icon></v-btn>
              <v-btn fab color="#0a3158"><v-icon>mdi-format-list-bulleted-square</v-icon></v-btn>
        
            </div>
            <div class="icons"></div>
              </v-col>
      </v-row>

            <div class="ourServices">
              <h1>Our Services</h1>
      <v-row justify="center">
        <v-col cols="12" md="3" justify="center" align="center">
              <div class="about">
                  <img src="../assets/worker.jpg" alt="">
                  <h2>Our people</h2>
                  <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque, nt optio a necessitatibus inventore eligendi non mollitia nam!</p> 
      <v-row justify="center">
                  <v-btn
                    color="success"
                    class="mt-12"
                    @click="overlay = !overlay"
                  >
                    Read More
                  </v-btn>

                  <v-overlay
                    :absolute="absolute"
                    :value="overlay"
                  >
                <v-card height="700"
                  width="800"
                  class="form">
                <v-btn
                        icon
                        @click="overlay = false"
                      >
                <v-icon class="close">mdi-close</v-icon>
              </v-btn>
             </v-card>
        </v-overlay>
      </v-row>
            </div>
          </v-col> 
       
          <v-col cols="12" md="3" justify="center" align="center">
            <div class="about">
              <img src="../assets/cargos.jpg" alt="">
              <h2>Import</h2>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus molestias beaerunt quam!</p>
        <v-row justify="center">
              <v-btn
                color="success"
                class="mt-12"
                @click="overlay = !overlay"
              >
                Read More
              </v-btn>

              <v-overlay
                :absolute="absolute"
                :value="overlay"
              >
            <v-card height="700"
              width="800"
              class="form">
              <v-btn
                      icon
                      @click="overlay = false"
                    >
                <v-icon class="close">mdi-close</v-icon>
              </v-btn>
             </v-card>
        </v-overlay>
      </v-row>
              </div>
            </v-col>
         
            <v-col cols="12" md="3" justify="center" align="center">
              <div class="about">
                <img src="../assets/shipInPort.jpg" alt="">
                <h2>Ports </h2>
                <p>Lorem ipsum dolor sit ame=um impedit id. Itaque, quos?</p>
        <v-row justify="center">
                <v-btn
                  color="success"
                  class="mt-12"
                  @click="overlay = !overlay"
                >
                  Read More
                </v-btn>

                <v-overlay
                  :absolute="absolute"
                  :value="overlay"
                >
              <v-card height="700"
                width="800"
                class="form">
                <v-btn
                        icon
                        @click="overlay = false"
                      >
                <v-icon class="close">mdi-close</v-icon>
              </v-btn>
             </v-card>
        </v-overlay>
      </v-row>
            </div>
          </v-col>
        </v-row>
      </div>
    </v-app>
  </v-container>
</template>

<script>
 

export default {
  name: 'Home',
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
     background-position-y: -100px;
     position: relative;

     .button{
       position: absolute;
       top: 430px;
       left: 650px;
       height:50px;
     
    }
  }

  .picture{
    background-image: url(../assets/cargo.jpg);
    height: 200px;
    background-size: cover;
    background-position-y: -350px;
    opacity:0.5;

  }

  .icons{
    height:150px; 
    background-color: #ada0a0;
    // opacity:0.5;
  }

  .ourServices{

    h1{
      margin-left:230px;
      margin-top:50px;

    }

  .about{
    // width:150px;
    height:450px;
    padding-left:20px;
    padding-top:20px; 

    img{
      width:300px;
      }

    .readMoreButton{

      margin-left:150px;

      }

      .form{
        background-color: white;
      }

      .close{
        color:grey;
      }
    }
  }

   @media only screen and (max-width:600px){
      .cover{
        background-position-y: -150px;
        background-position-x:-150px;
      
      }
  }

  @media only screen and (max-width:600px){
    .picture{
      background-position-y: -150px;
        background-position-x:-150px;
      height:500px;
    }
  }

</style>
