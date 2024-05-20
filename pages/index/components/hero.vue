<template>
    <v-parallax src="https://i.pinimg.com/564x/45/be/d2/45bed291ef0f2aee6630107b593bf5ac.jpg">
      <v-row
        class="fill-height"
        align="center"
        justify="center"
      >
        <v-col class="text-center">
          <h1 class="display-2 mb-5">Bienvenido a mi Sitio</h1>
          <p class="subheading mb-5">Explora nuestro contenido y descubre más sobre nosotros.</p>
          <v-btn color="primary" @click="goToAbout" class="mr-4">Acerca de</v-btn>
          <v-btn color="primary" @click="goToProducts">Productos</v-btn>
        </v-col>
      </v-row>
    </v-parallax>
  </template>
  
  <script>
  export default {
    methods: {
      goToAbout() {
        // Aquí puedes definir la lógica para navegar a la página "Acerca de"
        console.log("Navegar a la página Acerca de");
      },
      goToProducts() {
        // Aquí puedes definir la lógica para navegar a la página de "Productos"
        console.log("Navegar a la página de Productos");
      }
    }
  };
  </script>
  
  <style scoped>
  .subheading {
    font-size: 1.5em;
  }
  </style>
  