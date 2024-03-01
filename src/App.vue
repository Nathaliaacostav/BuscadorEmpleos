<template>
  <div>
    <h1>Lista de Empleos</h1>
    <div class="row">
      <div class="col-md-4" v-for="(empleo, index) in empleos" :key="index">
        <Card :empleo="empleo" />
      </div>
    </div>
  </div>
</template>

<script>
import Card from './components/Card.vue';  
import Empresas from './data/Empresas.json'; 

export default {
  components: {
    Card
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
