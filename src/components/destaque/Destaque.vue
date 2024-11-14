<template>
    <v-carousel
      height="400"
      show-arrows
      cycle
      interval="5000"
    >
      <v-carousel-item
        v-for="(imagem, indice) in imagens"
        :key="indice"
      >
        <v-img :src="imagem" />
      </v-carousel-item>
    </v-carousel>
</template>

<script>
  import imagem01 from "../../assets/01.png";
  import imagem02 from "../../assets/02.png";
  import imagem03 from "../../assets/03.png";

  export default {
    name: "Destaque",
    data() {
      return {
        imagens: [
          imagem01,
          imagem02,
          imagem03,
        ],
      };
    },
  }
</script>

<style scoped>
  @import './Destaque.css';
</style>
