  <template>
    <v-app-bar app class="custom-app-bar">
      <v-toolbar-title class="app-title">IzziStocks</v-toolbar-title>
      <v-btn text class="nav-btn" @click="redirectTo('/')">Pagina Principal</v-btn>
      <v-btn text class="nav-btn" @click="redirectTo('/products')">Planes y servicios</v-btn>
      <v-btn text class="nav-btn" @click="redirectTo('/about')">sobre nosotros</v-btn>
      <v-spacer></v-spacer>
    </v-app-bar>
  </template>

  <script>
  export default {
    methods: {
      redirectTo(route) {
        this.$router.push(route);
      }
    }
  }
  </script>

  <style>
  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans:wght@400;500;700&display=swap');

  .custom-app-bar {
    background-color: white;
    opacity: 1; /* Ensure the app bar is not transparent */
    box-shadow: 0 2px 4px rgba(255, 255, 255, 0.1); 
    border-bottom: 1px solid #E0E0E0; 
    font-family: 'Noto Sans', sans-serif; 
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 16px; 
    height: 64px; /* Standard height for app bars */
    z-index: 1000; /* Ensure it appears above other content */
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
    text-transform: none;
    transition: color 0.3s ease, text-decoration 0.3s ease;
  }

  .nav-btn:hover {
    background-color: transparent;
    text-decoration: underline;
    color: #8c7ae6;
    cursor: pointer;
  }
  </style>
    