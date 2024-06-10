<template>
  <div>
    <v-card
      class="mx-auto pa-12 pb-8 custom-card"
      elevation="8"
      max-width="448"
      rounded="lg"
    >
      <h1 class="headline text-center">Registro</h1>

      <v-text-field
        density="compact"
        placeholder="Nombre"
        prepend-inner-icon="mdi-account-outline"
        variant="outlined"
        class="custom-text-field"
      ></v-text-field>

      <v-text-field
        density="compact"
        placeholder="Apellido"
        prepend-inner-icon="mdi-account-outline"
        variant="outlined"
        class="custom-text-field"
      ></v-text-field>

      <v-text-field
        density="compact"
        placeholder="Correo Electrónico"
        prepend-inner-icon="mdi-email-outline"
        variant="outlined"
        class="custom-text-field"
      ></v-text-field>

      <div class="text-subtitle-1 text-medium-emphasis d-flex align-center justify-space-between">
        Contraseña
      </div>

      <v-text-field
        :append-inner-icon="visible ? 'mdi-eye-off' : 'mdi-eye'"
        :type="visible ? 'text' : 'password'"
        density="compact"
        placeholder="Ingresa tu contraseña"
        prepend-inner-icon="mdi-lock-outline"
        variant="outlined"
        class="custom-text-field"
        @click:append-inner="visible = !visible"
      ></v-text-field>

      <v-btn
        class="mb-8 custom-btn"
        size="large"
        variant="tonal"
        @click="redirectTo('/products')"
      >
        Registrarse
      </v-btn>

      <v-card-text class="text-center">
        <a
          class="text-blue text-decoration-none"
          href="javascript:void(0);"
          @click="redirectTo('/login')"
        >
          ¿Ya tienes una cuenta? Inicia sesión <v-icon icon="mdi-chevron-right"></v-icon>
        </a>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      visible: false
    };
  },
  methods: {
    redirectTo(route) {
      this.$router.push(route);
    }
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans:wght@400;500;700&display=swap');

.headline {
  font-family: 'Noto Sans', cursive, sans-serif;
  color: #3E2723;
}

.custom-card {
  background-color: white;
  border: 1px solid #E0E0E0;
}

.custom-text-field .v-input__control {
  font-family: 'Noto Sans', cursive, sans-serif;
}

.custom-btn {
  background-color: #8c7ae6;
  color: white;
  font-family: 'Noto Sans', cursive, sans-serif;
}
</style>
