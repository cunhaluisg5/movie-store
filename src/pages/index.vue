<template>
  <div class="fixo">
    <Cabecalho />
  </div>
  <div class="conteudo">
    <Menu />
    <Destaque />
    <Recentes />
  </div>
</template>

<script setup>
  import Cabecalho from "../components/Cabecalho/Cabecalho.vue";
  import Menu from "../components/menu/Menu.vue";
  import Destaque from '../components/destaque/Destaque.vue';
  import Recentes from "../components/recentes/Recentes.vue";
</script>

<style scoped>
  @import "./index.css"
</style>
