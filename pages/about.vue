<template>
  <v-app>
    <v-app-bar app class="custom-app-bar">
      <v-toolbar-title class="app-title">IzziStocks</v-toolbar-title>
      <v-btn text class="nav-btn" @click="redirectTo('/')">PÁGINA PRINCIPAL</v-btn>
      <v-btn text class="nav-btn" @click="redirectTo('/products')">PLANES Y SERVICIOS</v-btn>
      <v-btn text class="nav-btn" @click="redirectTo('/about')">SOBRE NOSOTROS</v-btn>
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-main>
      <v-container class="about-container" fluid>
        <v-row align="center" justify="space-between">
          <v-col cols="12" sm="6">
            <div class="text-content">
              <h1 class="headline">Sobre Nosotros</h1>
              <p>
                Somos una empresa especializada en sistemas de ventas e inventario, comprometidos con brindar soluciones innovadoras y de alta calidad para nuestros clientes.
              </p>
              <h2 class="subheadline">Nuestra Misión</h2>
              <p>
                Nuestra misión es brindar soluciones efectivas y personalizadas para nuestros clientes, ayudándolos a mejorar su eficiencia y productividad en la gestión de sus ventas e inventario.
              </p>
              <h2 class="subheadline">Nuestra Visión</h2>
              <p>
                Nuestra visión es ser líderes en el mercado de sistemas de ventas e inventario, conocidos por nuestra excelencia en la entrega de soluciones innovadoras y de alta calidad.
              </p>
            </div>
          </v-col>
          <v-col cols="12" sm="6">
            <v-img src="https://source.unsplash.com/random/800x600" class="project-image"></v-img>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'About',
  methods: {
    redirectTo(route) {
      this.$router.push(route);
    }
  }
}
</script>


<style scoped>
.custom-app-bar {
  background-color: #ffffff;
  box-shadow: none;
  border-bottom: none;
  font-family: 'Noto Sans', sans-serif;
}

.app-title {
  color: #8c7ae6; /* Cambia el color del logo */
  font-weight: 700;
  font-size: 1.5rem;
}

.v-spacer {
  flex: 1;
}

.nav-btn {
  color: #000000;
  font-weight: 500;
  text-transform: uppercase;
  transition: color 0.3s ease, text-decoration 0.3s ease;
}

.nav-btn:hover {
  background-color: transparent;
  text-decoration: underline;
  color: #8c7ae6;
  cursor: pointer;
}

.about-container {
  padding: 50px 20px;
}

.text-content {
  max-width: 600px;
  font-family: 'Noto Sans', sans-serif; /* Cambio de tipo de letra */
}

.headline {
  color: #000000;
  font-weight: 700;
  margin-bottom: 20px;
  font-size: 2.5rem;
}

.subheadline {
  color: #000000;
  font-weight: 500;
  margin-top: 30px;
  margin-bottom: 15px;
  font-size: 1.8rem;
}

p {
  color: #555;
  line-height: 1.6;
  margin-bottom: 20px;
}

.project-image {
  width: 100%;
  height: auto;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.project-image:hover {
  transform: translateY(-5px);
}
</style>
