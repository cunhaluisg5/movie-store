<template>
  <v-carousel
      :cycle="false"
      show-arrows
      hide-delimiters
    >
      <v-carousel-item
        v-for="(pagina, indice) in paginas"
        :key="indice"
      >
        <div class="d-flex justify-center align-center flex-wrap">
          <div
            v-for="(objeto, index) in pagina"
            :key="index"
            class="item"
          >
            <div class="titulo text-truncate">{{ objeto.titulo }}</div>
            <v-img :src="objeto.imagem" class="d-flex justify-center align-center" />
            <div class="valor">R$ {{ objeto.valor.toFixed(2) }}</div>
          </div>
        </div>
      </v-carousel-item>
    </v-carousel>
</template>

<script>
  import imagemRitualBluray from "../../assets/ritual-bluray.png";
  import imagemToyStory3Dvd from "../../assets/toy-story-3-dvd.png";
  import imagemAsAventurasDePiDvd from "../../assets/as-aventuras-de-pi-dvd.png";
  import imagemOsIncriveis2BlurayBluray3d from "../../assets/os-incriveis-2-bluray-bluray3d.png";
  import imagemAlien8PassageiroDvd from "../../assets/alien-8-passageiro-dvd.png";
  import imagemHobbitUmaJornadaInesperadaBluray from "../../assets/hobbit-uma-jornada-inesperada-bluray.png";

  export default {
    name: "Recentes",
    data() {
      return {
        listagem: [
          {
            titulo: "BLU-RAY - O RITUAL",
            valor: 34.90,
            imagem: imagemRitualBluray
          },
          {
            titulo: "DVD - TOY STORY 3",
            valor: 4.90,
            imagem: imagemToyStory3Dvd
          },
          {
            titulo: "DVD - AS AVENTURAS DE PI",
            valor: 4.90,
            imagem: imagemAsAventurasDePiDvd
          },
          {
            titulo: "BLURAY/BLURAY 3D - OS INCRÍVEIS 2",
            valor: 19.90,
            imagem: imagemOsIncriveis2BlurayBluray3d
          },
          {
            titulo: "DVD - ALIEN O 8° PASSAGEIRO",
            valor: 7.90,
            imagem: imagemAlien8PassageiroDvd
          },
          {
            titulo: "BLURAY - HOBBIT UMA JORNADA INESPERADA",
            valor: 16.90,
            imagem: imagemHobbitUmaJornadaInesperadaBluray
          }
        ],
      }
    },
    computed: {
      paginas() {
        const paginas = [];
        for (let i = 0; i < this.listagem.length; i += 4) {
          paginas.push(this.listagem.slice(i, i + 4));
        }
        return paginas;
      }
    }
  }
</script>

<style scoped>
  @import "./Recentes.css";
</style>
