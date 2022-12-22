<template>
  <div v-for="item in 7" class="flex flex-col-7">
    <div
      id="dias"
      class="border-2 border-slate-500 mt-2 hover:bg-sky-100 mx-5 h-20 rounded-lg"
    >
      <h1 class="font-bold ml-2 mt-1">{{ item }}</h1>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
#dias {
  box-shadow: 0px 0px 3px black;
}
</style>
