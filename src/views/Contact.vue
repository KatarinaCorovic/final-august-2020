<template>
    <v-container fluid>
        <v-app class="cover">
            <h1>Contact Us</h1>
                <v-row justify="center" align="center" > 
                        <div class="infodivs">
                    <v-col cols="12" md="6"  justify="center" align="center">
                        <div class="customerInfo">
                                <h2>Send us a message</h2>
                            <v-form>
                                <v-row>
                                    <v-col cols="12" md="5">
                                    <v-text-field regular label="Your Name" placeholder="Regine Phalange" >
                                        </v-text-field> 
                                    </v-col>
                                    <v-col cols="12" md="6">
                                        <v-text-field regular label="Email Address" placeholder="reginaphalange@gamil.com" >
                                        </v-text-field> 
                                    </v-col>
                                </v-row>
                                <v-row>
                                    <v-col cols="12" md="5">
                                        <v-text-field regular label="Phone" placeholder="(800) 800 - 900 - 100" >
                                        </v-text-field> 
                                    </v-col>
                                    <v-col cols="12" md="5">
                                        <v-text-field regular label="Company" placeholder="Magna" >
                                        </v-text-field> 
                                    </v-col>
                                </v-row>
                                <v-row>
                                    <v-col cols="12" md="6">
                                        <v-text-field regular label="Message" placeholder="Hello, I would like to talk about..." >
                                        </v-text-field>
                                    </v-col>
                                    <v-col cols="12" md="5">
                                <v-btn class="mx-2 sendButton" fab dark small color="#00b2ff"><v-icon>mdi-send</v-icon></v-btn>
                                </v-col>
                                </v-row>
                        </v-form>
                    </div>
                    </v-col>
                    <v-col cols="12" md="6" justify="center" align="center">
                    <div v-for="(info, index) in information" :key="index" class="contactInfo">
                    <h2>{{info.title}}</h2>
                    <p><v-icon>mdi-map-marker</v-icon> {{info.address}}</p>
                    <p><v-icon>mdi-phone</v-icon>  {{info.number}}</p>
                    <p><v-icon>mdi-email</v-icon>  {{info.email}}</p>
                            <v-card-text>
                    <v-btn
                        v-for="icon in icons"
                        :key="icon"
                        class="mx-1"
                        icon
                    >
                        <v-icon size="20px">{{ icon }}</v-icon>
                    </v-btn>
                    </v-card-text>
                    </div>
                    </v-col>
                    </div>
            </v-row>
        </v-app>
    </v-container>
</template>



<script>
export default {
    name:'Contact',
    data(){
        return{
            information:[

                {
                    title:'Contact Information',
                    address: '540 Seville Ferdinand Scorlese Da 123423',
                    number:'3343524525',
                    email:'magnacarta@gmail.com'
                }
            ],

             icons: [
                 
                    'mdi-facebook',
                    'mdi-twitter',
                    'mdi-linkedin',
                    'mdi-instagram',
             ],

             customerInfo:[
                 {
                     title:'Send us a Message',
                     nameTag:'Your name',
                     name:'Dexter Morgan',
                     phoneTag:'phone',
                     phone:'(800) 800 - 900 - 100',
                     messageTag:'Message',
                     message:'Hello, I would like to talk about...'


                 }
             ]
        }
    }
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
    //  opacity:0.5;

h1{
    color:white;
    font-size: 50px;
    text-align: center;
    padding-top:50px;
    font-weight: normal;
   }
}

   .infodivs{
    //    position:absolute;
    //    top:270px;
    //    left:370px;
       display: flex;
    //    margin-top:250px;
    //    margin-top:300px;

       
   }

.customerInfo{

    width:500px;
    height:400px;
    background-color: rgb(240, 240, 240);
    opacity:1;
    padding-left:20px;  
    
    h2{
        padding:20px 0 20px 0;
        text-align:left;
        font-weight: normal;
    }


     .sendButton{
         margin-top:50px;
         
     }

   }

.contactInfo{
     width:300px;
    height:400px;
    background-color: #0a3158;


h2{
    padding-top:30px;
    color:white;
}

p{
    padding-top:30px;
    color:white;

}

.sendButton{
    border-radius: 50%;
}
}


@media only screen and (max-width:600px){
     .cover{
         display:block;

     }
 }

@media only screen and (max-width:600px){
     .infodivs{
         display:block;

     }
 }

 @media only screen and (max-width:600px){
     .customerInfo{
         width:450px;
         height:700px;

     }
 }

  @media only screen and (max-width:600px){
     .customerInfo{
         width:450px;
         height:700px;

     }
 }

   @media only screen and (max-width:600px){
     .contactInfo{
         width:450px;
         
     }
 }




</style>