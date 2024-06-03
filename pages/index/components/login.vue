<template>
    <v-container>
      <v-row justify="center">
        <v-col cols="12" md="6">
          <v-card>
            <v-card-title>Iniciar Sesión</v-card-title>
            <v-card-text>
              <v-form>
                <v-text-field label="Correo Electrónico" v-model="email" type="email" required></v-text-field>
                <v-text-field label="Contraseña" v-model="password" type="password" required></v-text-field>
                <v-btn @click="login">Iniciar Sesión</v-btn>
              </v-form>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  export default {
    data() {
      return {
        email: '',
        password: ''
      };
    },
    methods: {
      login() {
        // Lógica de inicio de sesión aquí
        console.log('Iniciando sesión con', this.email, this.password);
      }
    }
  };
  </script>
  