<template>
    <v-container fluid pa-0>
        <v-app class="cover" >
            <h1>Contact Us</h1>
            <v-row justify="center" align="center"> 
                <v-col cols="12" md="4"  justify="center" align="center">
                    <div class="customerInfo">
                        <div class="sentInfo" v-if="visibility">
                            <h2 class="mt-3">Your order:</h2><br/>
                            <v-row>
                                <v-col cols="12" md="6">
                                    <h3>Your name: </h3>
                                    <p>{{name}}</p>
                                </v-col>
                                <v-col cols=12 md="6">
                                    <h3>Address: </h3>
                                    <p>{{address}}</p>
                                </v-col>
                            </v-row>
                            <v-row>
                                <v-col cols=12 md="6">  
                                    <h3>Phone number: </h3>
                                    <p>{{phone}}</p>
                                </v-col>
                                <v-col cols=12 md="6">
                                    <h3>Companies name: </h3>
                                    <p>{{company}}</p>
                                </v-col>
                                <v-row>
                                    <v-col cols=12 md="6">
                                        <h3>Message: </h3>
                                        <p>{{message}}</p>
                                    </v-col>
                                </v-row>
                            </v-row>
                        </div>
                            <h2>Send us a message</h2>
                            <v-form class="form" ref="form" v-model="valid" lazy-validation>
                                <v-row>
                                    <v-col cols="12" md="5">
                                        <v-text-field regular label="Your Name"
                                        placeholder="Regine Phalange"
                                        :rules="[v => !!v || 'This field is required',
                                        v => (v && v.length <= 10) || 'Name must be less than 10 characters']"
                                        required
                                        v-model="name" >
                                        </v-text-field> 
                                    </v-col>
                                    <v-col cols="12" md="6">
                                        <v-text-field regular label="Email Address"
                                        placeholder="reginaphalange@gamil.com"
                                        :rules="[v => !!v || 'This field is required',
                                        v => /.+@.+\..+/.test(v) || 'E-mail must be valid']"
                                        required
                                        v-model="address" >
                                        </v-text-field> 
                                    </v-col>
                                </v-row>
                                <v-row>
                                    <v-col cols="12" md="5">
                                        <v-text-field regular label="Phone"
                                        placeholder="(800) 800 - 900 - 100"
                                        :rules="[v => !!v || 'This field is required']"
                                        required
                                        v-model="phone" >
                                        </v-text-field> 
                                    </v-col>
                                    <v-col cols="12" md="5">
                                        <v-text-field regular label="Company"
                                        placeholder="Magna"
                                        :rules="[v => !!v || 'This field is required']"
                                        required
                                        v-model="company" >
                                        </v-text-field> 
                                    </v-col>
                                </v-row>
                                <v-row>
                                    <v-col cols="12" md="6">
                                        <v-text-field regular label="Message"
                                        placeholder="Hello, I would like to talk about..."
                                        :rules="[v => !!v || 'This field is required']"
                                        required
                                        v-model="message" >
                                        </v-text-field>
                                    </v-col>
                                    <v-col cols="12" md="5">
                                        <v-btn  @click="validate" :class="{ red: !valid, green: valid }" class="mx-2 sendButton" fab dark small color="#00b2ff"><v-icon>mdi-send</v-icon></v-btn>
                                    </v-col>
                                </v-row>
                            </v-form>
                        </div>
                </v-col>
                <v-col cols="12" md="3" justify="center" align="center">
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
            </v-row>
        </v-app>
    </v-container>
</template>



<script>
import axios from "axios";

export default {
    name:'Contact',
    data(){
        return{
            visibility:false,   
            valid: true,
            information:[

                {
                    title:'Contact Information',
                    address: '540 Seville Ferdinand Scorlese 123423',
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

        }
    },

methods:{
   validate () {
    var messageForm = this.$refs.form.validate()
    if(messageForm == true){
    this.submit()
    this.visibility = true;

    
    }
},

submit(){
    axios
    .post('http://localhost:8087/messages', {
        messageData:{
            id:null,
            name:this.name,
            address:this.address,
            phone:this.phone,
            company:this.company,
            message:this.message,
            
        }
    })

    .then(function(response){
        console.log(response.data)
    })
    .catch(function (error){
        console.log(error)
    })
        
  }
}

}
</script>

<style scoped lang="scss">

.cover {
    background-image: url(../assets/cargoship.jpg);
    background-repeat: no-repeat;
    position: relative;
    background-size: cover;
    background-size: 100%;

} 
h1  {
    color:white;
    font-size: 50px;
    text-align: center;
    padding-top:50px;
    font-weight: normal;
    
}
.customerInfo {
    width:500px;
    min-height:400px;
    background-color: rgb(240, 240, 240);
    opacity:1;
    padding-left:20px;
    

h2{
    padding:20px 0 20px 0;
    text-align:left;
    font-weight: normal;
}

.sendButton {
    margin-top:50px;
         
}
     
}

.sentInfo {
    border:1px solid black;
    background-color: #164370;
    z-index:1;
    position:absolute;
    top:205px;
    left:280px;
    height:400px;
    width:800px;
    color:white;    

h2 {
    text-align: center;
}
p {
    color:rgb(196, 187, 187);
}
}

.contactInfo {
    width:300px;
    min-height:400px;
    background-color: #0a3158;
   

h2  {
    padding-top:30px;
    color:white;
}

p {
    padding-top:30px;
    color:white;

}

.sendButton { 
    border-radius: 50%; 
}

}

</style>