<template>
  <div>
    <NavBar />
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-1">
          <SideBar />
        </div>
        <div class="col-md-11 ps-0">
          <div class="row">
            <div class="col-md-12 ps-0 sticky-search-bar m-0">
              <SearchBar class="" />
            </div>
          </div>
          <div class="row card-style">
            <div
              class="col-md-12 ps-3"
              v-for="(empleo, index) in empleos"
              :key="index"
            >
              <Card :empleo="empleo" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Card from "./components/Card.vue";
import SideBar from "./components/SideBar.vue";
import Empresas from "./data/Empresas.json";
import NavBar from "./components/NavBar.vue";
import SearchBar from "./components/SearchBar.vue";

export default {
  components: {
    Card,
    SideBar,
    NavBar,
    SearchBar,
  },
  data() {
    return {
      empleos: Empresas.empleos,
    };
  },
};
</script>

<style scoped>
.card-style {
  background-color: rgb(243, 245, 247);
  opacity: 1;
}

.sticky-search-bar {
  position: -webkit-sticky;
  position: sticky;
  top: 0;
  z-index: 1000;
  background-color: white;
}
</style>
