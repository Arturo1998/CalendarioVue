<template>
  <div class="container mx-auto">
    <div class="flex justify-center">
      <button class="rounded-full bg-sky-500 w-10 h-10" @click="abierto = true">
        <img src="../assets/icono+.png" alt="" class="" />
      </button>

      <div
        v-if="abierto"
        class="absolute inset-0 flex items-center justify-center bg-gray-700 bg-opacity-50"
      >
        <div class="ml-3 mr-3 p-6 bg-white rounded-md shadow-xl">
          <div class="flex items-center justify-between">
            <h3 class="text-2xl">Añade tu evento</h3>
            <svg
              @click="abierto = false"
              xmlns="http://www.w3.org/2000/svg"
              class="w-8 h-8 text-red-900 cursor-pointer"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M10 14l2-2m0 0l2-2m-2 2l-2-2m2 2l2 2m7-2a9 9 0 11-18 0 9 9 0 0118 0z"
              />
            </svg>
          </div>
          <div class="">
            <h1>Título</h1>
            <input type="text" />
            <h1>Descripción</h1>
            <input type="text" />
            <h1>Fecha</h1>
            <input type="date" />
          </div>
          <div class="mt-4">
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
