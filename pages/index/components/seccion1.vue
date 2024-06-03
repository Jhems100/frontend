<template>
  <v-container>
    <!-- Línea separadora antes de Características Principales -->
    <v-divider></v-divider>

    <!-- Características Principales -->
    <v-row justify-center class="section">
      <v-col cols="12" class="text-center">
        <h2 class="headline">Características Principales</h2>
        <v-row>
          <v-col cols="12" sm="4">
            <v-card class="custom-card">
              <v-card-title class="custom-card-title">Gestión Centralizada</v-card-title>
              <v-card-text class="custom-card-text">
                Unifica todo tu inventario en una sola plataforma
              </v-card-text>
            </v-card>
          </v-col>
          <v-col cols="12" sm="4">
            <v-card class="custom-card">
              <v-card-title class="custom-card-title">Registro de Transacciones</v-card-title>
              <v-card-text class="custom-card-text">
                Registra todas las transacciones de forma clara y precisa
              </v-card-text>
            </v-card>
          </v-col>
          <v-col cols="12" sm="4">
            <v-card class="custom-card">
              <v-card-title class="custom-card-title">Informes Financieros</v-card-title>
              <v-card-text class="custom-card-text">
                Genera informes financieros detallados para una mejor toma de decisiones
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-col>
    </v-row>

    <v-divider></v-divider>

    <!-- Por qué elegir nuestro sistema de inventario -->
    <v-container class="section text-center d-flex flex-column align-center justify-center">
      <v-row class="d-flex justify-center">
        <v-col cols="12">
          <h2 class="headline">¿Por qué elegir nuestro sistema de inventario?</h2><br>
          <v-row class="d-flex justify-center">
            <v-col cols="12" md="7">
              <v-card class="custom-card">
                <v-card-text>
                  <h3 class="headline">Eficiencia Mejorada</h3>
                  <p>Con funcionalidades automatizadas y una interfaz fácil de usar, nuestro sistema te permite ahorrar tiempo y recursos en la gestión de inventario.</p>
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>

    <v-divider></v-divider>

    <!-- Reposición Impecable -->
    <v-container class="section text-center">
      <v-row>
        <v-col cols="12">
          <h2 class="headline">Reposición Impecable</h2>
          <p>Mantén tu inventario siempre en óptimas condiciones con Izzistocks. Nuestro plan maestro de producción y estrategias de reposición automática aseguran que nunca te quedes sin stock. Automatizamos el seguimiento a proveedores, enviando mensajes y confirmando órdenes de compra, para una gestión eficiente y sin contratiempos.</p>
        </v-col>
      </v-row>
    </v-container>

    <v-row justify="center">
      <v-col cols="12" md="8" class="text-center">
        <v-img src="https://i.pinimg.com/736x/5e/a3/b6/5ea3b68c4291fe3953b1d28bec5ace88.jpg" alt="Proceso de Reposición" max-width="100%"></v-img>
      </v-col>
    </v-row>

    <v-divider></v-divider>

    <!-- Nuestro proyecto -->
    <v-container class="section text-center">
      <v-row>
        <v-col cols="12">
          <h2 class="headline">Nuestro proyecto</h2>
          <p>Nuestro sistema de inventario es la herramienta perfecta para optimizar la gestión de tus productos y llevar tu negocio al siguiente nivel. Además de unificar tu inventario, registrar transacciones y generar informes financieros, te proporciona una eficiencia mejorada para ahorrar tiempo y recursos. ¡Únete a cientos de empresas que ya han experimentado el poder de una gestión de inventario eficiente con nosotros!</p>
        </v-col>
      </v-row>
    </v-container>

    <!-- Línea separadora después de Nuestro proyecto -->
    <v-divider></v-divider>
  </v-container>
</template>

<script>
export default {
  name: 'InventoryPage',
  // Puedes agregar lógica adicional aquí si es necesario
}
</script>

<style scoped>
/* Estilos personalizados para esta página */
.headline {
  font-family: 'Noto Sans', sans-serif;
  color: #3E2723;
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.section {
  margin: 50px 0;
}

.custom-card {
  background-color: #F3E5F5;
  border: 1px solid #8E44AD;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.custom-card:hover {
  transform: translateY(-5px);
}

.custom-card-title {
  font-family: 'Noto Sans', sans-serif;
  color: #8E44AD;
  font-weight: bold;
}

.custom-card-text {
  font-family: 'Noto Sans', sans-serif;
  color: #5D4037;
}

p {
  font-family: 'Noto Sans', sans-serif;
  color: #3E2723;
  line-height: 1.6;
  margin-bottom: 20px;
}

.text-center {
  text-align: center;
}

.v-divider {
  margin: 30px 0;
  border-color: #8E44AD;
}
</style>
