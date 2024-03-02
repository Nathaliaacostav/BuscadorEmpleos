<script setup></script>

<template>
  <div class="container-fluid ">
    <nav class="navbar navbar-expand-lg bg-light pe-5">
      <div class="container-fluid">
        <img
          src="../../public/peackuImg.png"
          class="col-1 float-start mx-2"
          style="max-height: 75px; max-width: 75px"
          alt="..."
        />
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse justify-content-end" id="navbarSupportedContent">
          <div class="d-flex align-items-center  ">
            <ul class="navbar-nav col-11">
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="#"
                  >Empleos</a
                >
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Bootcamp</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Sobre nosotros</a>
              </li>
              <li class="nav-item dropdown">
                <a
                  class="nav-link dropdown-toggle"
                  href="#"
                  role="button"
                  data-bs-toggle="dropdown"
                  aria-expanded="false"
                >
                  Para profesionales
                </a>
                <ul class="dropdown-menu"></ul>
              </li>
              <li class="nav-item dropdown">
                <a
                  class="nav-link dropdown-toggle"
                  href="#"
                  role="button"
                  data-bs-toggle="dropdown"
                  aria-expanded="false"
                >
                  Para empresas
                </a>
                <ul class="dropdown-menu"></ul>
              </li>
              <button class="btn btn-light border rounded me-2" type="button" id="Español">
                <svg data-v-3b0d2ab4="" viewBox="0 0 16 16" width="1em" height="1em" focusable="false" role="img" aria-label="globe" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class=" bi-globe mr-1 b-icon bi" style="font-size: 120%;"><g data-v-3b0d2ab4=""><path d="M0 8a8 8 0 1 1 16 0A8 8 0 0 1 0 8zm7.5-6.923c-.67.204-1.335.82-1.887 1.855A7.97 7.97 0 0 0 5.145 4H7.5V1.077zM4.09 4a9.267 9.267 0 0 1 .64-1.539 6.7 6.7 0 0 1 .597-.933A7.025 7.025 0 0 0 2.255 4H4.09zm-.582 3.5c.03-.877.138-1.718.312-2.5H1.674a6.958 6.958 0 0 0-.656 2.5h2.49zM4.847 5a12.5 12.5 0 0 0-.338 2.5H7.5V5H4.847zM8.5 5v2.5h2.99a12.495 12.495 0 0 0-.337-2.5H8.5zM4.51 8.5a12.5 12.5 0 0 0 .337 2.5H7.5V8.5H4.51zm3.99 0V11h2.653c.187-.765.306-1.608.338-2.5H8.5zM5.145 12c.138.386.295.744.468 1.068.552 1.035 1.218 1.65 1.887 1.855V12H5.145zm.182 2.472a6.696 6.696 0 0 1-.597-.933A9.268 9.268 0 0 1 4.09 12H2.255a7.024 7.024 0 0 0 3.072 2.472zM3.82 11a13.652 13.652 0 0 1-.312-2.5h-2.49c.062.89.291 1.733.656 2.5H3.82zm6.853 3.472A7.024 7.024 0 0 0 13.745 12H11.91a9.27 9.27 0 0 1-.64 1.539 6.688 6.688 0 0 1-.597.933zM8.5 12v2.923c.67-.204 1.335-.82 1.887-1.855.173-.324.33-.682.468-1.068H8.5zm3.68-1h2.146c.365-.767.594-1.61.656-2.5h-2.49a13.65 13.65 0 0 1-.312 2.5zm2.802-3.5a6.959 6.959 0 0 0-.656-2.5H12.18c.174.782.282 1.623.312 2.5h2.49zM11.27 2.461c.247.464.462.98.64 1.539h1.835a7.024 7.024 0 0 0-3.072-2.472c.218.284.418.598.597.933zM10.855 4a7.966 7.966 0 0 0-.468-1.068C9.835 1.897 9.17 1.282 8.5 1.077V4h2.355z"></path></g></svg> <span style="font-size:.9em">Español     </span>         </button>
              <button class="btn btn-light border rounded" type="button"><svg data-v-8f85bb14="" viewBox="0 0 16 16" width="1em" height="1em" focusable="false" role="img" aria-label="bell" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi-bell b-icon bi"><g data-v-8f85bb14=""><path d="M8 16a2 2 0 0 0 2-2H6a2 2 0 0 0 2 2zM8 1.918l-.797.161A4.002 4.002 0 0 0 4 6c0 .628-.134 2.197-.459 3.742-.16.767-.376 1.566-.663 2.258h10.244c-.287-.692-.502-1.49-.663-2.258C12.134 8.197 12 6.628 12 6a4.002 4.002 0 0 0-3.203-3.92L8 1.917zM14.22 12c.223.447.481.801.78 1H1c.299-.199.557-.553.78-1C2.68 10.2 3 6.88 3 6c0-2.42 1.72-4.44 4.005-4.901a1 1 0 1 1 1.99 0A5.002 5.002 0 0 1 13 6c0 .88.32 4.2 1.22 6z"></path></g></svg></button>              
            </ul> 
              <button class="btn btn-light " type="button"><div class="row d-flex align-items-center">
                <div class="col-5">     
                  <div style="background-color: rgb(52, 58, 64); color:white;margin-left:-20px; width: 1.7em; height: 1.7em; border-radius: 50%; display: flex; justify-content: center; align-items: center;">
  <svg viewBox="0 0 16 16" width="1em" height="1em" fill="currentColor" class="bi-person b-icon bi rounded-fill" xmlns="http://www.w3.org/2000/svg">
    <path d="M8 8a3 3 0 1 0 0-6 3 3 0 0 0 0 6zm2-3a2 2 0 1 1-4 0 2 2 0 0 1 4 0zm4 8c0 1-1 1-1 1H3s-1 0-1-1 1-4 6-4 6 3 6 4zm-1-.004c-.001-.246-.154-.986-.832-1.664C11.516 10.68 10.289 10 8 10c-2.29 0-3.516.68-4.168 1.332-.678.678-.83 1.418-.832 1.664h10z"></path>
  </svg>
</div>
  
                </div>
                <div class="col-3 min-font d-flex ">
                  <div class="row ">
                    <div class="row">Juan </div>

                    <div class="col-6">               
                      <div class="row">Juan </div>
                      <div class="row">6780 </div>
                    </div>
                  </div>
                </div>
              </div>            
            </button>
         
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<style>
nav{
  font-size: .9em;
}
.min-font{
  font-size: .6em;
}

</style>
