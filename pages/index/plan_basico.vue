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
              <h1 class="custom-card-title">Plan Básico</h1>
              <p class="custom-card-text">
                Gestión de Productos<br>
                - Agregar Productos: Permite a los usuarios agregar nuevos productos al inventario.<br>
                - Editar Productos: Facilita la actualización de la información de los productos existentes.<br>
                - Eliminar Productos: Opción para eliminar productos que ya no están en inventario.<br>
                <br>
                Gestión de Inventario<br>
                - Control de Stock: Seguimiento del nivel de stock de cada producto.<br>
                - Alertas de Stock Bajo: Notificaciones cuando el inventario de un producto está por debajo de un nivel mínimo.<br>
                - Historial de Inventario: Registro de movimientos de inventario (entradas y salidas).<br>
                <br>
                Gestión de Ventas<br>
                - Registro de Ventas: Permite registrar cada venta realizada.<br>
                - Facturación Básica: Generación de facturas simples para los clientes.<br>
                - Reporte de Ventas: Acceso a reportes básicos sobre ventas realizadas en un período específico.<br>
                <br>
                Gestión de Clientes<br>
                - Agregar Clientes: Posibilidad de agregar nuevos clientes al sistema.<br>
                - Historial de Compras: Registro de las compras realizadas por cada cliente.<br>
                <br>
                Reportes y Análisis<br>
                - Reporte de Inventario: Reporte del estado actual del inventario.<br>
                - Reporte de Ventas: Reporte de ventas diarias, semanales o mensuales.<br>
                - Reporte de Clientes: Información sobre la frecuencia y volumen de compras de los clientes.<br>
                <br>
                Accesos y Permisos<br>
                - Usuario Único: El plan básico puede estar limitado a un único usuario administrador.<br>
                <br>
                Soporte y Actualizaciones<br>
                - Soporte Básico: Acceso a soporte técnico limitado (por ejemplo, solo vía email).<br>
                - Actualizaciones: Acceso a actualizaciones básicas del sistema.<br>
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
