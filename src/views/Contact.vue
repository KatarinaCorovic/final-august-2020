<template>
    <v-app>
        <v-row>
            <v-col cols="12">
                <div class="cover">
                    <h1>Contact Us</h1>
                </div>
            </v-col>
        </v-row>  
         <v-row jutify="center" align="center" class="infodivs"> 
            <v-col cols="12" md="4" jutify="center" align="center">
                <div class="contactInfo"></div>
            </v-col>
            <v-col cols="12" md="4" jutify="center" align="center">
                <div class="contact"></div>
            </v-col>
        </v-row>

    </v-app>
</template>



<script>
export default {
    name:'Contact'
}
</script>

<style scoped lang="scss">

  .cover{
     
     background-image: url(../assets/cargoship.jpg);
     min-height: 500px;
     background-size: cover;
     background-position-y: -350px;
     position: relative;
     opacity:0.5;

h1{
    color:white;
    font-size: 50px;
    text-align: center;
    padding-top:50px;
}
   }

   .infodivs{
       position:absolute;
       top:300px;
       right:250px;
       
   }

.contactInfo{

    width:400px;
    height:400px;
    background-color: rgb(218, 60, 60);
    opacity:1;
    padding-left:20px;  
    


   }

.contact{
    width:400px;
    height:400px;
    background-color: rgb(218, 60, 60);
    opacity:1;


}

</style>