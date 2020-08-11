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
        <!-- <div class="place">
          <h1>Where we are</h1>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ofprovident dignissimos qui? Sed vs qudantium aut.</p>
        </div> -->
    </v-row>




    <!-- <v-row justify="center">
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
          </v-card>
        </v-overlay>
      </v-row>
               -->
 
    </v-app>
  </v-container>
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