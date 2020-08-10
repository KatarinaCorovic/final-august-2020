<template>
  <v-container fluid>
    <v-app>
      <v-row>
       <v-col cols="12">
          <div class="cover">
            <v-btn depressed color="#ffb32a" class="button">PLACE THE ORDER</v-btn>
          </div>
            <i class="fas fa-ship"></i>
            <div class="picture"></div>
            <div class="icons"></div>
        </v-col>
      </v-row>

      <div class="ourServices">
        
      <v-row justify="center">
        <v-col cols="12" md="3" justify="center" align="center">
          <div class="about">
            <img src="../assets/worker.jpg" alt="">
            <h2>Cao</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque, nt optio a necessitatibus inventore eligendi non mollitia nam!</p> 
              <v-btn
                color="success"
                class="mt-12 readMoreButton " 
                @click="overlay = !overlay"
                  >
               Read More
              </v-btn>

              <v-overlay
                :absolute="absolute"
                :value="overlay"
              >
              <v-card height="700" width="800">
                    <v-overlay :value="overlay">
              <v-btn
                icon
                @click="overlay = false"
              >
                <v-icon>mdi-close</v-icon>
              </v-btn>
              </v-overlay>
              </v-card>
                </v-overlay>
      
          </div>
          </v-col> 
       
          <v-col cols="12" md="3" justify="center" align="center">
          <div class="about">
            <img src="../assets/worker.jpg" alt="">
            <h2>Hello</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus molestias beaerunt quam!</p>
            <v-btn
                color="success"
                class="mt-12 readMoreButton" 
                @click="overlay = !overlay"
                  >
               Read More
              </v-btn>

              <v-overlay
                :absolute="absolute"
                :value="overlay"
              >
              <v-card height="700" width="800">
                    <v-overlay :value="overlay">
              <v-btn
                icon
                @click="overlay = false"
              >
                <v-icon>mdi-close</v-icon>
              </v-btn>
              </v-overlay>
              </v-card>
                </v-overlay>
            </div>
            </v-col>
         
            <v-col cols="12" md="3" justify="center" align="center">
          <div class="about">
            <img src="../assets/worker.jpg" alt="">
            <h2>Mrvica</h2>
            <p>Lorem ipsum dolor sit ame=um impedit id. Itaque, quos?</p>
                    <v-btn
                        color="success"
                        class="mt-12 readMoreButton" 
                        @click="overlay = !overlay"
                          >
                      Read More
                      </v-btn>

                      <v-overlay
                        :absolute="absolute"
                        :value="overlay"
                      >
                      <v-card height="700" width="800">
                            <v-overlay :value="overlay">
                      <v-btn
                        icon
                        @click="overlay = false"
                      >
                        <v-icon>mdi-close</v-icon>
                    </v-btn>
                  </v-overlay>
                </v-card>
              </v-overlay>
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
     background-position-y: -350px;
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
    min-height: 200px;
    background-size: cover;
    background-position-y: -350px;
    opacity:0.5;

  }

  .icons{
     
    min-height:150px; 
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
    }
  }

</style>
