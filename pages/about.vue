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
      <v-container fluid>
        <v-row justify="center">
          <v-col cols="12" sm="8">
            <v-card class="custom-card elevation-12">
              <v-img
                src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
                height="200"
                gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              >
                <v-container fill-height fluid>
                  <v-row justify="center" align="center">
                    <v-col>
                      <h1 class="headline white--text mb-2">Sobre Nosotros</h1>
                      <div class="caption white--text">Conoce más sobre nuestra empresa</div>
                    </v-col>
                  </v-row>
                </v-container>
              </v-img>

              <v-card-text>
                <p class="headline">Quiénes Somos</p>
                <p>
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed vulputate, nisl ac malesuada sodales, justo ex convallis lorem, quis tempus purus libero sed dui. Aliquam vel vestibulum turpis. In hac habitasse platea dictumst.
                </p>
                <p>
                  Nulla facilisi. Nullam id urna vel nisi suscipit gravida. Morbi scelerisque vestibulum tellus vel consectetur. Integer in tellus vitae ante volutpat vestibulum. Donec eget odio justo. Integer maximus fringilla nulla a ullamcorper.
                </p>
              </v-card-text>
            </v-card>
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
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans:wght@400;500;700&display=swap');

.custom-app-bar {
  background-color: white;
  opacity: 1;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  border-bottom: 1px solid #E0E0E0;
  font-family: 'Noto Sans', sans-serif;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 16px;
  height: 64px;
  z-index: 1000;
}

.app-title {
  color: #8c7ae6;
  font-weight: 700;
  font-size: 1.25rem;
}

.v-spacer {
  flex: 1;
}

.nav-btn {
  color: #681919;
  font-weight: 500;
  text-transform: uppercase; /* Transform text to uppercase */
  transition: color 0.3s ease, text-decoration 0.3s ease;
}

.nav-btn:hover {
  background-color: transparent;
  text-decoration: underline;
  color: #8c7ae6;
  cursor: pointer;
}

.headline {
  font-family: 'Comic Sans MS', cursive, sans-serif;
  color: #3E2723;
}

.custom-card {
  background-color: #F3E5F5;
  border: 1px solid #8E44AD;
}

.caption {
  font-family: 'Comic Sans MS', cursive, sans-serif;
  color: #5D4037;
}

.v-card-text p {
  font-family: 'Comic Sans MS', cursive, sans-serif;
  color: #3E2723;
}
</style>
