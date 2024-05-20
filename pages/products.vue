<template>
  <v-app>
    <v-app-bar app color="primary">
      <v-toolbar-title>My App</v-toolbar-title>
      <v-btn text @click="redirectTo('/')">Home</v-btn>
      <v-btn text @click="redirectTo('/products')">Products</v-btn>
      <v-btn text @click="redirectTo('/about')">About</v-btn>
    </v-app-bar>

    <v-main>
      <v-container>
        <v-card class="mx-auto" max-width="344">
          <v-img
            height="200px"
            src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
            cover
          ></v-img>

          <v-card-title>
            Top western road trips
          </v-card-title>

          <v-card-subtitle>
            1,000 miles of wonder
          </v-card-subtitle>

          <v-card-actions>
            <v-btn color="orange-lighten-2" text>Explore</v-btn>

            <v-spacer></v-spacer>

            <v-btn :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'" @click="show = !show"></v-btn>
          </v-card-actions>

          <v-expand-transition>
            <div v-show="show">
              <v-divider></v-divider>

              <v-card-text>
                I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.
              </v-card-text>
            </div>
          </v-expand-transition>
        </v-card>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    show: false,
  }),
  methods: {
    redirectTo(route) {
      this.$router.push(route);
    }
  }
}
</script>

<style scoped>
.v-container {
  padding-top: 20px;
}
</style>
