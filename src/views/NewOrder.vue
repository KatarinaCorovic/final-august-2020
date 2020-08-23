<template>
    <v-container fluid pa-0>
        <v-app class="cover">
            <v-row justify="center" align="center">
                <v-col cols="12" md="6" justify="center" align="center">
                    <div class="formDiv">
                        <div class="sentForm" v-if="visibility">
                            <h1 class="mt-3">Your order:</h1><br/>
                            <v-row>
                                <v-col cols=12 md="6">
                                    <h2>Ship name: </h2>
                                    <p>{{shipName}}</p>
                                </v-col>
                            </v-row>
                            <v-row>
                                <v-col cols=12 md="6">
                                    <h2>Departure port: </h2>
                                    <p>{{dePort}}</p>
                                </v-col>
                                <v-col cols=12 md="6">  
                                    <h2>Arrival port: </h2>
                                    <p>{{arPort}}</p>
                                </v-col>
                            </v-row>
                            <v-row>
                                <v-col cols=12 md="6">
                                    <h2>Number of cargo: </h2>
                                    <p>{{number}}</p>
                                </v-col>
                                <v-col cols=12 md="6">
                                    <h2> Type of cargo: </h2>
                                    <p>{{type}}</p>
                                </v-col>
                            </v-row>
                            <v-row>
                                <v-col cols=12 md="6">
                                    <h2>Departure date: </h2>
                                    <p>{{depDate}}</p>
                                </v-col>
                                <v-col cols=12 md="6">
                                    <h2>Arrival date: </h2>
                                    <p>{{arDate}}</p>
                                </v-col>
                            </v-row>
                        </div>
                        <h1>Fill in the form{{formInfo}}</h1>
                        <div v-for="(value, index) in formInfo" v-bind:key="index">
                            <div>{{value.name}}{{index}}</div>
                        </div>
                        <v-form class="form" ref="form" v-model="valid" lazy-validation>
                            <v-row>
                                <v-col cols=12 md="6">
                                    <div class="input">
                                        <v-text-field solo label="Ship name" 
                                        prepend-inner-icon="mdi-pen" 
                                        autofocus="true" 
                                        :rules="[v => !!v || 'This field is required']"
                                        required
                                        v-model="shipName"
                                        ></v-text-field>
                                    </div>
                                </v-col>
                            </v-row>
                            <v-row>
                                <v-col cols="12" md="6">
                                    <div class="input">
                                        <v-text-field solo  
                                        label="Departure Port"
                                        prepend-inner-icon="mdi-map-marker"
                                        :rules="[v => !!v || 'This field is required']"
                                        required
                                        v-model="dePort"
                                        ></v-text-field>
                                    </div>
                                </v-col>
                                <v-col cols="12" md="6">
                                    <div class="input">
                                        <v-text-field solo 
                                        label="Arrival Port"
                                        prepend-inner-icon="mdi-map-marker" 
                                        :rules="[v => !!v || 'This field is required']"
                                        required
                                        v-model="arPort"
                                        ></v-text-field>
                                    </div>
                                </v-col>
                            </v-row>
                            <v-row>
                                <v-col cols="12" md="6">
                                    <div class="input">
                                        <v-text-field solo
                                        label="Number of cargo"
                                        prepend-inner-icon="mdi-plus"
                                        :rules="[v => !!v || 'This field is required']"
                                        required
                                        v-model="number"
                                        ></v-text-field>  
                                    </div>
                                </v-col>
                                <v-col cols="12" md="6">
                                    <div class="input">
                                        <v-text-field solo
                                        label="Type of cargo"
                                        prepend-inner-icon="mdi-pen"
                                        :rules="[v => !!v || 'This field is required']"
                                        required
                                        v-model="cargo"
                                        ></v-text-field>
                                    </div>
                                </v-col>
                            </v-row>
                            <v-row>
                                <v-col cols="12" md="6">
                                    <div class="input">
                                        <v-text-field solo
                                        label="Departure Date"
                                        prepend-inner-icon="mdi-calendar"
                                        :rules="[v => !!v || 'This field is required']"
                                        required
                                        v-model="depDate"
                                        ></v-text-field>
                                    </div>
                                </v-col>
                                <v-col cols="12" md="6">
                                    <div class="input">
                                        <v-text-field solo
                                        label="Arrival Date"
                                        prepend-inner-icon="mdi-calendar"
                                        :rules="[v => !!v || 'This field is required']"
                                        required
                                        v-model="arDate"
                                        ></v-text-field>    
                                    </div>
                                </v-col>
                            </v-row>
                            <v-row justify="center" align="center">
                                <v-col cols="12" md="6">
                                    <v-btn @click="validate" :class="{ red: !valid, green: valid }" class="submitButton" >SUBMIT</v-btn>
                                </v-col >
                                <v-col cols="12" md="6">
                                  <v-btn
                                    color="error"
                                    class="mr-4"
                                    @click="reset"
                                    >
                                    Reset Form
                                    </v-btn>
                                </v-col>
                            </v-row>
                        </v-form>
                    </div>
                </v-col>
            </v-row>
        </v-app>
    </v-container>
</template>

<script>
import axios from 'axios'

export default {
    name:'NewOrders',
    data:function(){
        return{
            valid: true,
            visibility:false
    }

},

methods:{
    validate () {
    var form = this.$refs.form.validate()
    if(form == true){
    this.submitData()
    this.visibility = true;

    }
    
    
    },

    reset () {
    this.$refs.form.reset()
    },
},

submitData(){
    axios
    .post('http://localhost:8087/forms', {
        formData:{
            id:null,
            shipName:this.shipName,
            dePort:this.dePort,
            arPort:this.arPort,
            number:this.number,
            cargo:this.cargo,
            depDate:this.depDate,
            arDate:this.arDate
            
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
</script>

<style scoped lang="scss">

.cover {
    background-image: url(../assets/cargoship.jpg);
    background-repeat: no-repeat;
    position: relative;
    background-size: cover;
    background-size: 100%;
      
}

.formDiv {
    background-color: #f0aa29;
    padding:50px;
    color:black;
    border:1px solid black;
    margin-top:100px;
    z-index:2;
    position: relative;
     
  
h1 {
    padding-bottom: 30px;
}

.submitButton {
    height:45px;
    width:120px;

}
}

.sentForm {
    border:1px solid black;
    background-color: rgb(240, 234, 234);
    z-index:1;
    position:absolute;
    top:0;
    left:0;
    height:100%;
    width:100%;

p{
    color:grey;
}

 }



  
</style>