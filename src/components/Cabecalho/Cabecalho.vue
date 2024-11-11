<template>
  <v-row class="d-flex justify-center container pa-4" no-gutters>
    <!-- Coluna para o título -->
    <v-col class="d-flex justify-center align-center" :cols="12" :md="2">
      <h1>MOVIE STORE</h1>
    </v-col>

    <!-- Coluna para o campo de busca -->
    <v-col class="d-flex justify-center align-center" :cols="12" :md="4">
      <v-text-field
        :rules="rules"
        hide-details="auto"
        label="DIGITE O QUE VOCÊ PROCURA"
        class="input-text"
      />
      <v-icon left color="#c29453" class="lupa">mdi-magnify</v-icon>
    </v-col>

    <!-- Coluna "ATENDIMENTO" -->
    <v-col class="d-flex flex-row justify-center align-center" :cols="12" :md="2">
      <div class="circulo mr-1">
        <v-icon left color="#FFFFFF">mdi-phone</v-icon>
      </div>
      <div class="d-flex flex-column justify-center">
        <span class="titulo">ATENDIMENTO</span>
        <span>FALE CONOSCO</span>
      </div>
    </v-col>

    <!-- Coluna "MINHA CONTA" -->
    <v-col class="d-flex flex-row justify-center align-center" :cols="12" :md="2">
      <div class="circulo mr-1">
        <v-icon left color="#FFFFFF">mdi-account</v-icon>
      </div>
      <div class="d-flex flex-column justify-center">
        <span class="titulo">MINHA CONTA</span>
        <span>ACESSAR CONTA</span>
      </div>
    </v-col>

    <!-- Coluna "MEU CARRINHO" -->
    <v-col class="d-flex flex-row justify-center align-center" :cols="12" :md="2">
      <div class="circulo mr-1">
        <v-icon left color="#FFFFFF">mdi-cart</v-icon>
      </div>
      <div class="d-flex flex-column justify-center">
        <span class="titulo">MEU CARRINHO</span>
        <span>CARRINHO VAZIO</span>
      </div>
    </v-col>
  </v-row>
</template>

<script>
  export default {
    name: "Cabecalho"
  };
</script>

<style scoped>
  @import "./Cabecalho.css";
</style>
