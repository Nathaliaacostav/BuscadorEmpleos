<script setup>
import { ref } from "vue";

defineProps({
  msg: String,
});

const count = ref(0);
</script>

<template>
  <div class="card">
    <img  class="card-img-top" alt="..." />
    <div class="card-body">
      <h5 class="card-title">ejmplo</h5>
    </div>
  </div>
</template>

<style>
.read-the-docs {
  color: #888;
}
</style>
