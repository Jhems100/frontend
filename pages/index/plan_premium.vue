<template>
    <v-app>
      <v-app-bar app class="custom-app-bar" dense elevate-on-scroll>
        <v-toolbar-title class="app-title">IzziStocks</v-toolbar-title>
        <v-btn text to="/">Página Principal</v-btn>
        <v-btn text to="/products">Planes y servicios</v-btn>
        <v-btn text to="/about">Sobre nosotros</v-btn>
        <v-spacer></v-spacer>
        <v-btn icon @click="redirectTo('/login')" class="nav-btn">
          <v-icon color="#000000">mdi-account</v-icon>
        </v-btn>
      </v-app-bar>
  
      <v-main class="custom-main">
        <v-container>
          <v-row>
            <v-col cols="12" md="8" class="custom-card">
              <h1 class="custom-card-title">Plan Premium</h1>
              <p class="custom-card-text">
                1. Todas las Funcionalidades del Plan Básico y Avanzado<br>
                <br>
                2. Gestión de Productos y Inventario Premium<br>
                - Predicción de Inventario: Herramientas avanzadas para la predicción de necesidades de inventario basadas en datos históricos y tendencias.<br>
                - Gestión de Proveedores: Herramientas para gestionar y evaluar proveedores, incluyendo órdenes de compra automatizadas.<br>
                <br>
                3. Gestión de Ventas y Clientes Premium<br>
                - Gestión de Cuentas por Cobrar y Pagar: Seguimiento detallado de cuentas por cobrar y pagar.<br>
                - Marketing Automatizado: Herramientas de automatización de marketing, como email marketing y campañas dirigidas.<br>
                <br>
                4. Reportes y Análisis Avanzados<br>
                - Inteligencia de Negocios (BI): Herramientas de BI para análisis profundo y visualización de datos.<br>
                - Dashboard Personalizable: Panel de control altamente personalizable con métricas e indicadores clave de rendimiento (KPI).<br>
                <br>
                5. Automatización y Integraciones Premium<br>
                - Integración con Marketplaces: Conexión con marketplaces en línea como Amazon, eBay, etc.<br>
                - API Avanzada: Acceso a una API avanzada para integraciones personalizadas con otros sistemas.<br>
                <br>
                6. Usuarios y Permisos Premium<br>
                - Usuarios Ilimitados: Permitir un número ilimitado de usuarios.<br>
                - Gestión de Equipos: Herramientas avanzadas para la gestión de equipos y flujos de trabajo.<br>
                <br>
                7. Soporte y Actualizaciones Premium<br>
                - Soporte Dedicado: Acceso a un gestor de cuenta dedicado para soporte personalizado.<br>
                - Consultoría y Capacitación: Servicios de consultoría y capacitación personalizados.<br>
                - Actualizaciones Exclusivas: Acceso anticipado a nuevas funcionalidades y mejoras exclusivas para usuarios premium.<br>
                <br>
                8. Seguridad y Cumplimiento<br>
                - Copia de Seguridad Avanzada: Copias de seguridad automáticas y recuperación de datos.<br>
                - Cumplimiento Normativo: Herramientas para ayudar a cumplir con normativas y estándares específicos del sector.<br>
              </p>


            </v-col>
  
            <v-col cols="12" md="4">
              <v-row justify="center">
                <v-img 
                  :src="currentImage" 
                  alt="Imagen Plan Básico" 
                  max-width="400" 
                  class="plan-image custom-image-position"
                ></v-img>
              </v-row>
              <v-row justify="center">
                <v-btn outlined color="#8c7ae6" @click="redirectTo('/login')" class="buy-btn">Comprar Plan Basico</v-btn>
              </v-row>
            </v-col>
          </v-row>
  
          <v-row class="custom-back-button" justify="start">
            <v-btn outlined color="#8E44AD" to="/products" class="custom-back-btn">Volver a los Planes</v-btn>
          </v-row>
        </v-container>
      </v-main>
    </v-app>
  </template>
  
  <script>
  export default {
    name: 'PlanBasico',
    data() {
      return {
        images: [
          'https://i.pinimg.com/736x/9f/6a/b3/9f6ab3990fbaae9d76ae11dd0c0c1bed.jpg',
          'https://i.pinimg.com/736x/02/be/4a/02be4a32204180a232ad19b0f3691064.jpg',
          'https://i.pinimg.com/736x/b1/d6/22/b1d622d8c13178e462949fde2c95edf8.jpg'
        ],
        currentImageIndex: 0,
      };
    },
    computed: {
      currentImage() {
        return this.images[this.currentImageIndex];
      },
    },
    methods: {
      redirectTo(route) {
        this.$router.push(route);
      },
      // Método para cambiar a la siguiente imagen cada 3 segundos
      startImageSlider() {
        setInterval(() => {
          this.currentImageIndex = (this.currentImageIndex + 1) % this.images.length;
        }, 3000); // Cambia la imagen cada 3 segundos
      },
    },
    mounted() {
      // Inicia el cambio de imágenes cuando el componente está montado
      this.startImageSlider();
    },
  };
  </script>
  

<style scoped>
.custom-card {
  background-color: #F3E5F5;
  border: 1px solid #8E44AD;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
  padding: 20px;
  margin: 20px 0;
  border-radius: 8px;
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

.plan-image {
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.custom-app-bar {
  background-color: rgba(255, 255, 255, 0.95);
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);
}

.custom-main {
  margin-top: 64px; /* Ajustar según la altura del v-app-bar */
  margin-left: -100px;
}

.custom-back-button {
  margin-top: 20px;
}

.custom-back-btn {
  color: #8E44AD; /* Color del texto */
  border-color: #8E44AD; /* Color del borde */
  border-radius: 4px; /* Radio de borde */
  font-weight: bold; /* Peso de la fuente */
  transition: background-color 0.3s; /* Transición suave */
  margin: 10px; /* Margen */
}

.custom-back-btn:hover {
  background-color: #8E44AD; /* Cambia el color de fondo al pasar el ratón */
  color: #ffffff; /* Cambia el color del texto al pasar el ratón */
}

/* Nueva clase CSS para ajustar la posición de la imagen */
.custom-image-position {
  margin-top: 150px;
  margin-left: 150px;
  margin-right: -150px;
}

.buy-btn {
  margin-top: 30px;
  margin-left: 300px;
  color: white;
}
</style>

