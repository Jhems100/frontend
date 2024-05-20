<template>
    <v-app-bar app color="primary">
      <v-toolbar-title>IzziStocks</v-toolbar-title>
      <v-btn text @click="redirectTo('/')">Pagina Principal</v-btn>
      <v-btn text @click="redirectTo('/products')">Planes y servicios</v-btn>
      <v-btn text @click="redirectTo('/about')">Informacion</v-btn>
    </v-app-bar>
  </template>
  
  <script>
  export default {
    methods: {
      redirectTo(route) {
        this.$router.push(route);
      }
    }
  }
  </script>
  