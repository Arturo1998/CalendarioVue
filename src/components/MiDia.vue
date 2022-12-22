<template>
  <div v-for="item in 24">
    <div
      id="horas"
      class="border-1 border-slate-500 mt-2 hover:bg-orange-100 mx-5 h-20 rounded-lg"
      @click="mostrar"
    >
      <h1 class="font-bold ml-2 mt-1">{{ item }} : 00</h1>
    </div>
  </div>
</template>

<script setup>
function mostrar() {
  console.log("hola");
}
</script>

<style lang="scss" scoped>
#horas {
  box-shadow: 0px 0px 3px black;
}
</style>
