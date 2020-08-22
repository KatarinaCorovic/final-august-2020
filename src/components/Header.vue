<template>
  <v-toolbar color=#0a3158>
    <h1>MAGNA</h1>
    <img src="../assets/cargo-ship.png" alt="" class="ship">  
    <v-spacer></v-spacer>
      <nav class="d-none d-sm-flex">
        <router-link to="/"><span>HOME</span></router-link>  
        <router-link to="/about"><span>ABOUT US</span></router-link> 
        <router-link to="/newOrder"><span>NEW ORDER</span></router-link>
        <router-link to="/contact"><span>CONTACT</span></router-link>
      </nav>
      <div class="text-center d-sm-flex d-md-none">
    <v-menu offset-y>
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color=#0a3158
          dark
          v-bind="attrs"
          v-on="on"
        >
         <v-app-bar-nav-icon></v-app-bar-nav-icon>
        </v-btn>
      </template>
      <v-list>
        <v-list-item
          v-for="(item, index) in items"
          :key="index"
          router :to="item.route"
          
        >
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        
        </v-list-item>
      </v-list>
    </v-menu>
  </div>
  </v-toolbar>
</template>



<script>
export default {
    name:'Header',
      data: () => ({
      items: [
        { title: 'HOME', route:'/', },
        { title: 'ABOUT US', route:'/about', },
        { title: 'ORDERS LIST', route:'/newOrder', },
        { title: 'CONTACT', route:'/contact', },
      ],
    }),
  
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