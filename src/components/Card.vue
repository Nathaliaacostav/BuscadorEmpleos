<template>
  <div class="m-3 py-4 job-card border rounded shadow-sm p-3 mb-3">
    <div class=" ">
      <img
        :src="empleo.imagen"
        class="  col-1 rounded float-start "
        style="max-height: 65px; max-width: 65px;"
        alt="..."

      />
      <div class="col-10">
        <div class="row justify-content-start">
          <h5 class="col-md-4 fs-4 text-start">{{ empleo.cargo }}</h5>
          <div class="col-md-5">
            <ul class="list-inline ">
              <li
                v-for="(habilidad, index) in empleo.habilidades_requeridas"
                :key="index"
                class=" list-inline-item border rounded p-1 "
              >
                {{ habilidad }}
              </li>
            </ul>
          </div>
        </div>

        <div class="row justify-content-start">
          <p class="card-text col-md-2 text-start">
            {{ empleo.nombre_empresa }}
          </p>
          <p class="card-text col-2 text-start">{{ empleo.modalidad_trabajo }}</p>
          <p class="card-text col-2 text-start">{{ empleo.salario }}</p>
          <p class="card-text col-2 text-start">{{ empleo.vacantes }}</p>
          <p class="card-text col-2 text-start">{{ tiempoPublicacion }}</p>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import { formatDistanceToNow } from 'date-fns';

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
    }
  }
};
</script>

<style scoped>
.job-card{
  background-color: rgb(255, 255, 255);
  transition-property: color border;
filter:0;
transition: .5s ease ;

}
.job-card:hover{
  box-shadow: 40px 30px 50px 20px rgba(173, 112, 112, 0.5); 

filter: drop-shadow( 0 0 3rem rgb(164, 179, 226));
  }
</style>

