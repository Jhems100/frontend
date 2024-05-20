<template>
  <v-app>
    <v-app-bar app color="primary">
      <v-toolbar-title>IzziStocks</v-toolbar-title>
      <v-btn text @click="redirectTo('/')">pagina principal</v-btn>
      <v-btn text @click="redirectTo('/products')">Planes y servicios</v-btn>
      <v-btn text @click="redirectTo('/about')">sobre nosotros</v-btn>
    </v-app-bar>

    <v-main>
      <v-container fluid>
        <v-row justify="center">
          <v-col cols="12" sm="8">
            <v-card class="elevation-12">
              <v-img
                src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
                height="200"
                gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              >
                <v-container fill-height fluid>
                  <v-row justify="center" align="center">
                    <v-col>
                      <h1 class="display-2 white--text mb-2">About Us</h1>
                      <div class="caption white--text">Learn more about our company</div>
                    </v-col>
                  </v-row>
                </v-container>
              </v-img>

              <v-card-text>
                <p class="subtitle-1">Who We Are</p>
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
</style>
