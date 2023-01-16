<template>
  <div class="container mx-auto">
    <div class="flex justify-center">
      <button
        class="rounded-full bg-slate-700 w-10 h-10"
        @click="abierto = true"
      >
        <img src="../assets/icono+.png" alt="" class="" />
      </button>

      <div
        v-if="abierto"
        class="absolute w-auto h-auto inset-0 flex items-center justify-center bg-gray-700 bg-opacity-50 h-screen"
      >
        <div
          class="p-6 bg-gradient-to-t from-white via-sky-200 to-sky-500 rounded-md shadow-xl"
        >
          <div class="flex w-96 justify-center">
            <h3 class="text-2xl">Añade tu evento</h3>
          </div>
          <div class="mt-3">
            <h1>Título</h1>
            <input type="text" class="border-2 border-slate-400 w-96" />
            <h1>Descripción</h1>
            <input type="text" class="border-2 border-slate-400 w-96 h-20" />
            <div class="flex mt-4 ml-1 space-x-3 w-auto">
              <h1>Fecha</h1>
              <input type="date" class="border-2 border-slate-400" />
              <h1>Hora</h1>
              <input type="" class="border-2 border-slate-400 w-32" />
            </div>
          </div>
          <div class="mt-5 flex justify-center space-x-20">
            <button
              @click="abierto = false"
              class="px-6 py-2 text-sky-500 border border-sky-500 rounded"
            >
              Cerrar
            </button>
            <button class="px-6 py-2 ml-2 text-blue-100 bg-sky-500 rounded">
              Guardar
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
import { ref } from "vue";

let abierto = ref(false);
</script>
