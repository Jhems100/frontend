<template>
  <v-container>  
    <!-- Características Principales -->
    <v-row>
      <v-col cols="12">
        <h2 class="headline">Características Principales</h2>
        <v-list>
          <v-list-item-group>
            <v-list-item>
              <v-list-item-icon>
                <v-icon class="custom-icon">mdi-check-circle</v-icon>
              </v-list-item-icon>
              <v-list-item-content>
                <v-list-item-title>Gestión Centralizada</v-list-item-title>
                <v-list-item-subtitle>Unifica todo tu inventario en una sola plataforma</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
            <v-list-item>
              <v-list-item-icon>
                <v-icon class="custom-icon">mdi-check-circle</v-icon>
              </v-list-item-icon>
              <v-list-item-content>
                <v-list-item-title>Registro de Transacciones</v-list-item-title>
                <v-list-item-subtitle>Registra todas las transacciones de forma clara y precisa</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
            <v-list-item>
              <v-list-item-icon>
                <v-icon class="custom-icon">mdi-check-circle</v-icon>
              </v-list-item-icon>
              <v-list-item-content>
                <v-list-item-title>Informes Financieros</v-list-item-title>
                <v-list-item-subtitle>Genera informes financieros detallados para una mejor toma de decisiones</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
            <!-- Añadir más elementos de la lista según las características -->
          </v-list-item-group>
        </v-list>
      </v-col>
    </v-row>
    
    <!-- Por qué elegir nuestro sistema de inventario -->
    <v-row>
      <v-col cols="12">
        <h2 class="headline">¿Por qué elegir nuestro sistema de inventario?</h2>
        <v-row>
          <v-col cols="12" md="6">
            <v-card class="custom-card">
              <v-card-text>
                <h3 url ="headline">Eficiencia Mejorada</h3>
                <p>Con funcionalidades automatizadas y una interfaz fácil de usar, nuestro sistema te permite ahorrar tiempo y recursos en la gestión de inventario.</p>
              </v-card-text>
            </v-card>
          </v-col>
          <v-col cols="12" md="6">
            <!-- Añadir más tarjetas para cada punto de venta -->
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    
    <!-- Conclusión -->
    <v-row>
      <v-col cols="12">
        <h2 class="headline">Nuestro proyecto</h2>
        <p>Nuestro sistema de inventario es la herramienta perfecta para optimizar la gestión de tus productos y llevar tu negocio al siguiente nivel. Además de unificar tu inventario, registrar transacciones y generar informes financieros, te proporciona una eficiencia mejorada para ahorrar tiempo y recursos. ¡Únete a cientos de empresas que ya han experimentado el poder de una gestión de inventario eficiente con nosotros!</p>
      </v-col>
    </v-row>
    
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
  font-family: 'Comic Sans MS', cursive, sans-serif;
  color: #3E2723;
}

.custom-icon {
  color: #8E44AD;
}

.custom-card {
  background-color: #F3E5F5;
  border: 1px solid #8E44AD;
}

.v-list-item-title {
  font-family: 'Comic Sans MS', cursive, sans-serif;
}

.v-list-item-subtitle {
  color: #5D4037;
}

p {
  font-family: 'Comic Sans MS', cursive, sans-serif;
  color: #3E2723;
}

</style>
