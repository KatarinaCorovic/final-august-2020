<template>
  <v-app >
    <Header/>
    <div id="nav">
      <Cookie id="cookie"/>
      </div>
      <v-main>
      <router-view/>
      </v-main>
    <Footer/>
  </v-app>
</template>

<script>
import Header from './components/Header';
import Footer from './components/Footer';
import Cookie from './components/Cookie';
// import Axios from "axios";


export default {
  name: 'App',
  components: {
    Header,
    Footer,
    Cookie
    
  },

  data: function(){
       return {
//       lightMode:'light', 
//       buttonPosition:'lightMode', 
//       cookieObj:null,
//       cookieColorMode:null,
//       cookieButtonPosition:null
//     }
//   },
//   methods: {
//     lightModeSwitch(){
//       this.cookieObj = new this.$cookie
//       if(this.cookieButtonPosition == 'lightMode'){
  
//         this.cookieObj.create('colorMode','dark',10);
//         this.cookieColorMode = this.cookieObj.read('colorMode')

       
//         this.cookieObj.create('buttonPosition','darkMode',10);
//         this.cookieButtonPosition = this.cookieObj.read('buttonPosition')
//       } else {
       
//         this.cookieObj.create('colorMode','light',10);
//         this.cookieColorMode = this.cookieObj.read('colorMode')

        
//         this.cookieObj.create('buttonPosition','lightMode',10);
//         this.cookieButtonPosition = this.cookieObj.read('buttonPosition')
//       }
//     }
//   },
//   mounted(){
//     this.cookieObj = new this.$cookie;

//     this.cookieColorMode = this.cookieObj.read('colorMode')
//     if(!this.cookieColorMode){
//       this.cookieObj.create('colorMode',this.lightMode,10)
//       this.cookieColorMode = this.cookieObj.read('colorMode') //setting the color to default light
//     }

//     this.cookieButtonPosition = this.cookieObj.read('buttonPosition')
//     if(!this.cookieButtonPosition){
//       this.cookieObj.create('buttonPosition',this.buttonPosition,10)
//       this.cookieButtonPosition = this.cookieObj.read('buttonPosition') //setting the button to default light
    }
  }
}

  

</script>

<style lang="scss">

body{
  margin:0;
  padding:0;

}

</style>
