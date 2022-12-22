<template>
  <div></div>
  <ModalAniadir />
  <MiCabecera />
  <MiDia />
</template>

<script setup>
import MiDia from "./components/MiDia.vue";
import MiCabecera from "./components/MiCabecera.vue";
import MiSemana from "./components/MiSemana.vue";
import ModalAniadir from "./components/ModalAniadir.vue";
import { ref } from "vue";
const vista = ref("");
</script>

<style lang="scss" scoped></style>
