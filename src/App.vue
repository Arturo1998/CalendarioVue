<template>
  <div>
    {{ eventos }}
    <div class="">
      <ModalAniadir />
    </div>
    <MiCabecera />
    <MiDia :eventos="eventos"/>
  </div>
</template>

<script setup>
import MiDia from "./components/MiDia.vue";
import MiCabecera from "./components/MiCabecera.vue";
import ModalAniadir from "./components/ModalAniadir.vue";
import { ref, onMounted } from "vue";
import axios from "axios";
import dayjs from "dayjs";
const vista = ref("");
const eventos = ref([]);

onMounted (() => {
  console.log(getEventos());
})
  async function getEventos() {
    try{
     const response = await axios.get("http://localhost:3000/eventos");
      eventos.value = response.data;
    }catch(e){
      console.log(e);
    }
  }
  
 const diaActual=ref(dayjs);

</script>

<style lang="scss" scoped></style>
