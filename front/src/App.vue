<script setup>
  import {ref, computed } from 'vue'
  import Inicio from './views/inicio.vue'
  import Lista from './views/lista.vue'
  import Cadastro from './views/cadastro.vue'
  import Editar from './views/editar.vue'

  const  routes = {
    '/': Inicio,
    '/ListadeAnimes': Lista,
    '/CadastrodeAnimes': Cadastro,
    '/EditarAnimes': Editar
  }

  const currentPath = ref(window.location.hash)

  window.addEventListener('hashchange', ()=>{
    currentPath.value = window.location.hash
  })

  const currentView = computed(() => {
    return routes[currentPath.value.slice(1) || '/']
  })

</script>

<template>
  <component  :is="currentView" />
</template>

<style>
@import "tailwindcss";
</style>

