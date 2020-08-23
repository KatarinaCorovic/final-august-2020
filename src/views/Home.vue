<template>
  <v-container fluid class="pa-0 ">
    <v-app>
      <v-row>
        <v-col cols="12" class="pa-0 ma-0">
          <div class="cover">
            <div class="button">
              <router-link to="/newOrder"><v-btn depressed color="#ffb32a" class="orderBtn">PLACE AN ORDER</v-btn></router-link>
            </div>
          </div>
          <div class="picture" >
            <div class="opacity"></div>
            <div class="icons">
              <v-btn fab color="#0a3158" class="iconBtn"><v-icon>mdi-domain</v-icon></v-btn>
              <v-btn fab color="#0a3158" class="iconBtn"><v-icon>mdi-vuetify</v-icon></v-btn> 
              <v-btn fab color="#0a3158" class="iconBtn"><v-icon>mdi-heart</v-icon></v-btn>
              <v-btn fab color="#0a3158" class="iconBtn"><v-icon>mdi-format-list-bulleted-square</v-icon></v-btn>
            </div>
          </div>
          <div class="plainColor ma-0 pa-0"></div>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12" md="6">
          <v-card
            class="mx-auto"
            max-width="400"
            tile
            >
            <v-toolbar color="#ce2a38">
              <v-icon>mdi-anchor</v-icon>
              <v-toolbar-title>List of ships departuring today:</v-toolbar-title>
            </v-toolbar>
              <v-list disabled>
                <v-list-item-group v-model="value" color="primary">
                  <v-list-item
                    v-for="(value, index) in shipInfo" v-bind:key="index"
                  >
                      <h3 v-text="value.shipName"></h3><v-spacer></v-spacer>
                      <h3 v-text="value.time_of_departure"></h3>
                  </v-list-item>
                </v-list-item-group>
              </v-list>
          </v-card>
        </v-col>
        <v-col cols="12" md="6">
          <v-card
            class="mx-auto"
            max-width="400"
            tile
            >
            <v-toolbar color="#ce2a38">
              <v-icon>mdi-anchor</v-icon>
              <v-toolbar-title>List of Ports opened today:</v-toolbar-title>
            </v-toolbar>
            <v-list disabled>
              <v-list-item-group v-model="value" color="primary">
                <v-list-item
                  v-for="(value, index) in portInfo" v-bind:key="index"
                >
                    <h3 v-text="value.name"></h3>
                </v-list-item>
              </v-list-item-group>
            </v-list>
          </v-card>
        </v-col>
      </v-row>
    </v-app>
  </v-container>
</template>

<script>
import axios from 'axios'
 

export default {
  name: 'Home',
   data:function(){
        return{

        shipInfo:{
            
        },

        portInfo:{

        },

  
        dateElements: {
        hour:'numeric',
        minute:'numeric'
        }
     }
  },

    mounted(){
        axios
        .get('http://localhost:8087/api/ships')
        .then(response =>{
            this.shipInfo = response.data

        })
        axios
        .get('http://localhost:8087/api/ports')
        .then(response =>{
            this.portInfo = response.data
           
        })
         
      }
  }


</script>

<style scoped lang="scss">

  .cover {
     background-image: url(../assets/cargoship.jpg);
     min-height: 550px;
     background-size: cover;
     background-position-y: -100px;
   
  }

.button {
    margin:0 auto;
    text-align:center;                   
    padding-top:400px;

a {
  text-decoration-style: none;

}
}

.picture {
    background-image: url(../assets/cargo.jpg);
    height: 200px;
    background-size: cover;
    background-position-y: -350px;
    position: relative;
    z-index: 2;

}

.opacity {
    position:absolute;
    top:0;
    left:0;
    height:100%;
    width:100%;
    background-color: rgba($color: #000000, $alpha: .5);
      
}

.icons {
  text-align:center;
  z-index: 1;
  padding-top:50px;
  
}

.plainColor {
    height:150px; 
    background-color: #ada0a0;
    
}

  
</style>
