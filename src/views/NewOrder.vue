<template>
    <v-container fluid>
        <v-app class="cover">
        
        <v-row justify="center" align="center">
            <v-col cols="12" md="6" justify="center" align="center">
                <div class="formDiv">
                    <h1>Fill in the form:</h1>
                <v-form class="form" >
                            <v-row>
                                <v-col cols=12 md="6">
                                    <div class="input">
                                        
                                        <v-text-field solo label="Ship name" 
                                        prepend-inner-icon="mdi-pen" 
                                        autofocus="true"></v-text-field>
                                    </div>
                                </v-col>
                            </v-row>
                            <v-row>
                                <v-col cols="12" md="6">
                                    <div class="input">
                                        
                                        <v-text-field solo  
                                        label="Departure Port"
                                        prepend-inner-icon="mdi-map-marker"
                                        ></v-text-field>
                                    </div>
                                </v-col>
                                <v-col cols="12" md="6">
                                    <div class="input">
                                    
                                        <v-text-field solo 
                                        label="Arrival Port"
                                        prepend-inner-icon="mdi-map-marker" 
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
                                ></v-text-field>  
                            </div>
                            </v-col>
                            <v-col cols="12" md="6">
                            <div class="input">
                                
                                <v-text-field solo
                                label="Type of cargo"
                                prepend-inner-icon="mdi-pen"  
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
                                ></v-text-field>
                            </div>
                        </v-col>
                        <v-col cols="12" md="6">
                            <div class="input">
                                
                                <v-text-field solo
                                label="Arrival Date"
                                prepend-inner-icon="mdi-calendar"
                                ></v-text-field>
                            </div>
                        </v-col>
                    </v-row>
                    <v-row justify="center" align="center">
                        <v-col cols="12" md="6">
                            <v-btn class="submitButton" >SUBMIT</v-btn>

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
export default {
    name:'NewOrders'
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
    //   opacity:0.5;
}

 .formDiv{
    //  position:absolute;
    //  top:100px;
    //  left: 400px;
     width:700px;
     height:700px;
     background-color: #f0aa29;
     padding:50px;
     color:black;
     border:1px solid black;
     margin-top:100px;
     
     
     
h1{
    padding-bottom: 30px;
}

.submitButton{
    height:45px;
    width:120px;

  }
 }
 @media only screen and (max-width:600px){
     .formDiv{
         width:450px;
         height:1000px;

     }
 }
  
 
</style>