<template>
  <div >
    
    <SearchBar/>
    <NavBar />
    <SideBar/>
   
    <div class="row">
      <div class="col-md-12" v-for="(empleo, index) in empleos" :key="index">
        <Card :empleo="empleo" />
      </div>
    </div>
    
  </div>
</template>

<script>
import Card from './components/Card.vue';  
import SideBar from './components/SideBar.vue';
import Empresas from './data/Empresas.json'; 
import NavBar from './components/NavBar.vue'
import SearchBar from './components/SearchBar.vue'


export default {
  components: {
    Card,
    SideBar, 
    NavBar,
    SearchBar
  },
  data() {
    return {
      empleos: Empresas.empleos 
    };
  }
};
</script>

<style scoped>
</style>
