<template>
  <div>
    <NavBar class="p-0" />
    <div class="container-fluid">
      <div class="row">
        <div class="col-1 px-0 mx-0 ">
          <SideBar class="h-100 sideBar" />
        </div>
        <div class="col-md-11 ps-0" style="position: relative;">
          <div class="row sticky-top">
            <div class="col-12 px-0">
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

.sideBar{
position: fixed;
}
</style>
