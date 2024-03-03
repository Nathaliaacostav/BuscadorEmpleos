<template>
  <div class="m-2 py-2 ps-3 job-card bordered rounded ">
    <div class="d-flex align-items-center ">
      <img
        :src="empleo.imagen"
        class="  col-1  float-start me-5 "
        style="max-height: 75px; max-width: 75px;"
        alt="..."

      />
      <div class="col-10 ">
        <div class="row d-flex align-items-start justify-content-start mb-2 ">
          <h6 class="col-4 fs-5 text-truncate text-start fw-bolder mb-0 ">{{ empleo.cargo }}</h6>
          <div class="col-md-5 d-flex justify-content-start ">
            <ul class="list-inline d-flex justify-content-start  mb-0  ">
              <li
                v-for="(habilidad, index) in empleo.habilidades_requeridas"
                :key="index"
                class="list-inline-item bordered-li px-2"
              >
                {{ habilidad }}
              </li>
            </ul>
          </div>
        </div>

        <div class="row justify-content-start">
          <p class="card-text col-md-2 text-start  text-dark fw-normal text-truncate mb-0 ps-0">
            <svg data-v-378c8849="" viewBox="0 0 16 16" width="1em" height="1em" focusable="false" role="img" aria-label="building" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi-building b-icon bi"><g data-v-378c8849=""><path fill-rule="evenodd" d="M14.763.075A.5.5 0 0 1 15 .5v15a.5.5 0 0 1-.5.5h-3a.5.5 0 0 1-.5-.5V14h-1v1.5a.5.5 0 0 1-.5.5h-9a.5.5 0 0 1-.5-.5V10a.5.5 0 0 1 .342-.474L6 7.64V4.5a.5.5 0 0 1 .276-.447l8-4a.5.5 0 0 1 .487.022zM6 8.694 1 10.36V15h5V8.694zM7 15h2v-1.5a.5.5 0 0 1 .5-.5h2a.5.5 0 0 1 .5.5V15h2V1.309l-7 3.5V15z"></path><path d="M2 11h1v1H2v-1zm2 0h1v1H4v-1zm-2 2h1v1H2v-1zm2 0h1v1H4v-1zm4-4h1v1H8V9zm2 0h1v1h-1V9zm-2 2h1v1H8v-1zm2 0h1v1h-1v-1zm2-2h1v1h-1V9zm0 2h1v1h-1v-1zM8 7h1v1H8V7zm2 0h1v1h-1V7zm2 0h1v1h-1V7zM8 5h1v1H8V5zm2 0h1v1h-1V5zm2 0h1v1h-1V5zm0-2h1v1h-1V3z"></path></g></svg> {{ empleo.nombre_empresa }}
          </p>
          <p class="card-text col-2 text-start mb-0"><svg data-v-378c8849="" viewBox="0 0 16 16" width="1em" height="1em" focusable="false" role="img" aria-label="geo alt" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi-geo-alt b-icon bi"><g data-v-378c8849=""><path d="M12.166 8.94c-.524 1.062-1.234 2.12-1.96 3.07A31.493 31.493 0 0 1 8 14.58a31.481 31.481 0 0 1-2.206-2.57c-.726-.95-1.436-2.008-1.96-3.07C3.304 7.867 3 6.862 3 6a5 5 0 0 1 10 0c0 .862-.305 1.867-.834 2.94zM8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10z"></path><path d="M8 8a2 2 0 1 1 0-4 2 2 0 0 1 0 4zm0 1a3 3 0 1 0 0-6 3 3 0 0 0 0 6z"></path></g></svg>{{ empleo.modalidad_trabajo }}</p>
          <p class="card-text col-2 text-start mb-0"><svg data-v-378c8849="" viewBox="0 0 16 16" width="1em" height="1em" focusable="false" role="img" aria-label="cash" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi-cash b-icon bi"><g data-v-378c8849=""><path d="M8 10a2 2 0 1 0 0-4 2 2 0 0 0 0 4z"></path><path d="M0 4a1 1 0 0 1 1-1h14a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1H1a1 1 0 0 1-1-1V4zm3 0a2 2 0 0 1-2 2v4a2 2 0 0 1 2 2h10a2 2 0 0 1 2-2V6a2 2 0 0 1-2-2H3z"></path></g></svg>{{ empleo.salario }}</p>
          <p class="card-text col-2 text-start mb-0"><svg data-v-378c8849="" viewBox="0 0 16 16" width="1em" height="1em" focusable="false" role="img" aria-label="people" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi-people b-icon bi"><g data-v-378c8849=""><path d="M15 14s1 0 1-1-1-4-5-4-5 3-5 4 1 1 1 1h8zm-7.978-1A.261.261 0 0 1 7 12.996c.001-.264.167-1.03.76-1.72C8.312 10.629 9.282 10 11 10c1.717 0 2.687.63 3.24 1.276.593.69.758 1.457.76 1.72l-.008.002a.274.274 0 0 1-.014.002H7.022zM11 7a2 2 0 1 0 0-4 2 2 0 0 0 0 4zm3-2a3 3 0 1 1-6 0 3 3 0 0 1 6 0zM6.936 9.28a5.88 5.88 0 0 0-1.23-.247A7.35 7.35 0 0 0 5 9c-4 0-5 3-5 4 0 .667.333 1 1 1h4.216A2.238 2.238 0 0 1 5 13c0-1.01.377-2.042 1.09-2.904.243-.294.526-.569.846-.816zM4.92 10A5.493 5.493 0 0 0 4 13H1c0-.26.164-1.03.76-1.724.545-.636 1.492-1.256 3.16-1.275zM1.5 5.5a3 3 0 1 1 6 0 3 3 0 0 1-6 0zm3-2a2 2 0 1 0 0 4 2 2 0 0 0 0-4z"></path></g></svg>{{ empleo.vacantes }} Vacante</p>
          <p class="card-text col-2 text-start mb-0 "><svg data-v-378c8849="" viewBox="0 0 16 16" width="1em" height="1em" focusable="false" role="img" aria-label="calendar3" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi-calendar3 b-icon bi"><g data-v-378c8849=""><path d="M14 0H2a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V2a2 2 0 0 0-2-2zM1 3.857C1 3.384 1.448 3 2 3h12c.552 0 1 .384 1 .857v10.286c0 .473-.448.857-1 .857H2c-.552 0-1-.384-1-.857V3.857z"></path><path d="M6.5 7a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm-9 3a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm-9 3a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2z"></path></g></svg>{{ tiempoPublicacion }}</p>
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
.job-card {
    background-color: rgb(255, 255, 255);
    transition-property: color border;
    filter: 0;
    transition: filter .5s ease;
}

.bordered {
    border: 1px solid rgb(231, 230, 230);
    border-radius: 30px;
}

.bordered-li {
    border: 1px solid black;
    border-radius: 30px;
}



.job-card:hover {
    filter: drop-shadow(rgb(214, 214, 214) -1rem 1rem .6rem);
}

svg {
    margin: 10px;
}

li{
  font-size: .8em;
}
p {
    display: flex;
    align-items: center;
    font-size: 0.9em;
}
</style>

