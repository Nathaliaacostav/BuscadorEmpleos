<template>
  <div class="row">
    <img
      :src="empleo.imagen"
      class="col-1 rounded float-start img-thumbnail"
      alt="..."
    />
    <div class="col-10">
      <div class="row">
        <h5 class="col-2">{{ empleo.cargo }}</h5>
        <div class="col-2">
          <ul class="list-inline">
            <li
              v-for="(habilidad, index) in empleo.habilidades_requeridas"
              :key="index"
              class="list-inline-item"
            >
              {{ habilidad }}
            </li>
          </ul>
        </div>
      </div>

      <div class="row">
        <p class="card-text col-1">{{ empleo.nombre_empresa }}</p>
        <p class="card-text col-1">{{ empleo.modalidad_trabajo }}</p>
        <p class="card-text col-1">{{ empleo.salario }}</p>
        <p class="card-text col-1">{{ empleo.vacantes }}</p>
        <p class="card-text col-1">{{ tiempoPublicacion }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import { formatDistanceToNow } from "date-fns";

export default {
  props: {
    empleo: {
      type: Object,
      required: true,
    },
  },
  computed: {
    tiempoPublicacion() {
      const horaPublicacion = new Date(this.empleo.hora_publicacion);
      return formatDistanceToNow(horaPublicacion, { addSuffix: true });
    },
  },
};
</script>

<style scoped>

</style>
