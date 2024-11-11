<template>
  <v-row class="d-flex justify-center container pa-4" no-gutters>
    <v-col
      v-for="(item, index) in menuItens"
      :key="index"
      class="d-flex justify-center align-center"
      :cols="3"
    >
      <a :href="item.link">{{ item.titulo }}</a>
    </v-col>
  </v-row>
</template>

<script>

export default {
  name: "Menu",
  setup() {
    const menuItens = [
      { titulo: "FILMES", link: "" },
      { titulo: "BLU-RAY", link: "" },
      { titulo: "DVD", link: "" },
      { titulo: "SOBRE", link: "" }
    ];

    return {
      menuItens
    };
  }
};
</script>

<style scoped>
  @import "./Menu.css";
</style>
