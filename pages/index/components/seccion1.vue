  <template>
    <v-container>  
      <!-- Características Principales -->
      <v-row justify-center>
    <v-col cols="12" class="text-center">
      <h2 class="headline">Características Principales</h2>
      <v-row>
        <v-col cols="12" sm="4">
          <v-list-item>
            <v-list-item-icon>
              <v-icon class="custom-icon">mdi-check-circle</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>Gestión Centralizada</v-list-item-title>
              <v-list-item-subtitle>Unifica todo tu inventario en una sola plataforma</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-col>
        <v-col cols="12" sm="4">
          <v-list-item>
            <v-list-item-icon>
              <v-icon class="custom-icon">mdi-check-circle</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>Registro de Transacciones</v-list-item-title>
              <v-list-item-subtitle>Registra todas las transacciones de forma clara y precisa</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-col>
        <v-col cols="12" sm="4">
          <v-list-item>
            <v-list-item-icon>
              <v-icon class="custom-icon">mdi-check-circle</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>Informes Financieros</v-list-item-title>
              <v-list-item-subtitle>Genera informes financieros detallados para una mejor toma de decisiones</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-col>
      </v-row>
    </v-col>
  </v-row>

      <!-- Por qué elegir nuestro sistema de inventario -->
      <v-container class="text-center d-flex flex-column align-center justify-center">
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
          <v-col cols="12" md="6">
            <!-- Añadir más tarjetas para cada punto de venta -->
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>


      <!-- Reposición Impecable -->
    <v-container class="text-center">
      <v-row>
        <v-col cols="12">
          <h2 class="headline">Reposición Impecable</h2>
          <p>Mantén tu inventario siempre en óptimas condiciones con Izzistocks. <br>Nuestro plan maestro de producción y estrategias de reposición automática <br> aseguran que nunca te quedes sin stock. Automatizamos el seguimiento a <br> proveedores, enviando mensajes y confirmando órdenes de compra,<br> para una gestión eficiente y sin contratiempos.</p>
        </v-col>
      </v-row>
      </v-container>

      <v-row justify="center">
        <v-col cols="12" md="8" class="text-center">
          <v-img src="/Users/jhemscalizayaicloud.com/Desktop/frontend/public/Captura de pantalla 2024-05-27 a la(s) 7.03.02 p. m..png" alt="Proceso de Reposición" max-width="100%"></v-img>
        </v-col>
      </v-row>
      
      <!-- Nuestro proyecto -->
      <v-container class="text-center">
      <v-row>
        <v-col cols="12">
          <h2 class="headline">Nuestro proyecto</h2>
          <p>Nuestro sistema de inventario es la herramienta perfecta para optimizar la gestión<br> de tus productos y llevar tu negocio al siguiente nivel. Además de unificar tu inventario,<br> registrar transacciones y generar informes financieros, te proporciona una eficiencia<br> mejorada para ahorrar tiempo y recursos. ¡Únete a cientos de empresas que ya <br>han experimentado el poder de una gestión de inventario eficiente con nosotros!</p>
        </v-col>
      </v-row>
    </v-container>
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

  .text-center {
    text-align: center;
  }
  </style>
