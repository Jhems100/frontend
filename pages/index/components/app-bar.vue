<template>
    <v-app-bar app color="primary">
      <v-toolbar-title>My App</v-toolbar-title>
      <v-btn text @click="redirectTo('/')">Home</v-btn>
      <v-btn text @click="redirectTo('/products')">Products</v-btn>
      <v-btn text @click="redirectTo('/about')">About</v-btn>
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
  