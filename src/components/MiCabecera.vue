<template>
  <div>
    <div
      id="fondo"
      class="h-16 bg-slate-900 rounded mt-1 mx-4 border-2 border-slate-700 flex"
    >
      <button
        class="bg-orange-100 rounded-full h-12 w-5 mt-1.5 ml-2 hover:bg-orange-500 border-2 border-slate-700"
      >&lt</button>
      <div class="m-auto rounded bg-orange-100 h-7 w-30 text-sm text-center">
        <h1 class="mt-1 mx-2">
          {{ dia.toDateString() }}
        </h1>
      </div>

      <button
        class="bg-orange-100 rounded-full h-12 w-5 mt-1.5 hover:bg-orange-500 border-2 mr-2 border-slate-700"
      >&gt</button>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import dayjs from "dayjs";
const dia = new Date();
</script>

<style lang="scss" scoped>
#fondo {
  box-shadow: 0px 0px 3px black;
}
</style>
