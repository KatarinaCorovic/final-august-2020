<template>
    <!-- <v-card
    color="grey lighten-4"
    flat
    height="200px"
    tile
  > -->
    <v-toolbar color=#0a3158>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <h1>MAGNA</h1>
      <img src="../assets/cargo-ship.png" alt="" class="ship">  

      <v-spacer></v-spacer>

         <nav>
              <router-link to="/"><span>HOME</span></router-link>  
              <router-link to="/about"><span>ABOUT US</span></router-link> 
              <router-link to="/newOrder"><span>ORDERS LIST</span></router-link>
              <router-link to="/contact"><span>CONTACT</span></router-link>
         </nav>
    </v-toolbar>
  <!-- </v-card>   -->
</template>



<script>
export default {
    name:'Header'
  
}
</script>


<style scoped lang="scss">

.toolbar{
  background-color: #0a3158;

  }
  
  h1{
    font-weight: lighter; 
    font-style: italic;
    font-family: "Adobe Arabic, serif";
    color:#FFD600;
    padding-right:10px;
}

.ship{
  width:30px;
  height:30px;
  

}

  nav a{
    padding: 0 15px;
    text-decoration: none;
    color:white;
  }

  nav a:hover {
  border-bottom: 1px solid white;
}



</style>