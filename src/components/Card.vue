<template>
    <div class="card">
      <img :src="empleo.imagen" class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">{{ empleo.cargo }}</h5>
        <p class="card-text">{{ empleo.nombre_empresa }}</p>
        <p class="card-text">{{ empleo.modalidad_trabajo }}</p>
        <p class="card-text">{{ empleo.salario }}</p>
        <p class="card-text">{{ empleo.vacantes }}</p>
        <p class="card-text">{{ empleo.hora_publicacion }}</p>
        <ul>
          <li v-for="(habilidad, index) in empleo.habilidades_requeridas" :key="index">{{ habilidad }}</li>
        </ul>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      empleo: {
        type: Object,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  /* Estilos específicos del componente */
  </style>
  