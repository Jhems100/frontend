<template>
    <div>
      <appbar></appbar>
      <hero></hero>
      <seccion1></seccion1>
      <carousel></carousel>
      <contact-form></contact-form>
    </div>
  </template>
  
  <script setup>
  import seccion1 from "./components/seccion1.vue"
  import appbar from "./components/app-bar.vue"
  import Hero from "./components/hero.vue"
  import ContactForm from "./components/contact.vue" // Importa el nuevo componente
  </script>
  