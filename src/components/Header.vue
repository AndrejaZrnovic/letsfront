<template>

  <v-toolbar color=#000000>
    <STYLE>A {text-decoration: none;} </STYLE>
     <router-link to="/"><v-btn fab color="#ffb32a" class="iconBtn"><v-icon>mdi-facebook-gaming</v-icon></v-btn></router-link>
     <router-link to="/"><h1>FLIX</h1></router-link>
    
    <v-spacer></v-spacer>
    <nav class="d-none d-sm-flex">
      <router-link to="/"><span>HOME</span></router-link>  
      <router-link to="/qalendar"><span>CALENDAR</span></router-link> 
      <router-link to="/treve"><span>SEARCH</span></router-link>
      <router-link to="/contact"><span>CONTACT</span></router-link>
    </nav>

  </v-toolbar>
</template>



<script>
export default {
    name:'Header',
      data: () => ({
      items: [
        { title: 'HOME', route:'/', },
        { title: 'CALENDAR', route:'/qalendar', },
        { title: 'SEARCH', route:'/treve', },
        { title: 'CONTACT', route:'/contact', },
      ],
    }),
  
}
</script>


<style scoped lang="scss">


  h1{
    // font-weight: lighter; 
    text-decoration: none;
    font-size: 60px;
    font-family: "Arial", sans-serif;
    color:white;
    padding: 10px;
}
  h1:hover{
    color: #ffa600;
  }

  nav a{
    padding: 0 15px;
    text-decoration: none;
    color:#ffff
  }

  nav a:hover {
  color: #ffa600;

}


</style>