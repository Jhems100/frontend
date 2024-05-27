<template>
  <v-app>
    <v-app-bar app color="primary">
      <v-toolbar-title>IzziStocks</v-toolbar-title>
      <v-btn text @click="redirectTo('/')">pagina principal</v-btn>
      <v-btn text @click="redirectTo('/products')">planes y servicios</v-btn>
      <v-btn text @click="redirectTo('/about')">sobre nosotros</v-btn>
    </v-app-bar>

    <div class="d-flex align-center justify-center fill-height">
      <v-container>
        <v-row class="mx-auto my-12" align="center" justify="center">
          <v-col cols="12" class="text-center">
            <h1 class="andale-mono">NUESTROS PLANES MENSUALES</h1>
          </v-col>
        </v-row>
        <v-row class="mx-auto my-12" align="center" justify="center" style="width: 100%;">
          <v-col cols="auto" class="card-col">
            <v-card :disabled="loading" :loading="loading" max-width="374">
              <template v-slot:loader="{ isActive }">
                <v-progress-linear :active="isActive" color="deep-purple" height="4" indeterminate></v-progress-linear>
              </template>

              <v-img height="250"
                src="public/el concepto del sistema de control de inventario, el gerente profesional y el trabajador están verificando el suministro de bienes y existencias, la gestión de inventario con la demanda de bienes.jpeg"
                cover></v-img>

              <v-card-item>
                <v-card-title>Plan Basico</v-card-title>

                <v-card-subtitle>
                  <span class="me-1">Sugerido</span>

                  <v-icon color="error" icon="mdi-fire-circle" size="small"></v-icon>
                </v-card-subtitle>
              </v-card-item>

              <v-card-text>
                <v-row align="center" class="mx-0">
                  <v-rating :model-value="4.5" color="amber" density="compact" size="small" half-increments
                    readonly></v-rating>

                  <div class="text-grey ms-4">
                    4.5 (413)
                  </div>
                </v-row>

                <div class="my-4 text-subtitle-1">
                  7$ • La paz, Bolivia
                </div>

                <div>Sistema para rastrear, gestionar y optimizar niveles de inventario empresarial.</div>
              </v-card-text>

              <v-divider class="mx-4 mb-1"></v-divider>

              <v-card-actions>
                <v-btn color="deep-purple-lighten-2" text="Comprar" block border @click="reserve"></v-btn>
              </v-card-actions>
            </v-card>
          </v-col>

          <v-col cols="auto" class="card-col">
            <v-card :disabled="loading" :loading="loading" max-width="374">
              <template v-slot:loader="{ isActive }">
                <v-progress-linear :active="isActive" color="deep-purple" height="4" indeterminate></v-progress-linear>
              </template>

              <v-img height="250"
                src="public/el concepto del sistema de control de inventario, el gerente profesional y el trabajador están verificando el suministro de bienes y existencias, la gestión de inventario con la demanda de bienes.jpeg"
                cover></v-img>

              <v-card-item>
                <v-card-title>Plan Avanzado</v-card-title>

                <v-card-subtitle>
                  <span class="me-1">Popular</span>

                  <v-icon color="error" icon="mdi-fire-circle" size="small"></v-icon>
                </v-card-subtitle>
              </v-card-item>

              <v-card-text>
                <v-row align="center" class="mx-0">
                  <v-rating :model-value="5" color="amber" density="compact" size="small" half-increments
                    readonly></v-rating>

                  <div class="text-grey ms-4">
                    5 (678)
                  </div>
                </v-row>

                <div class="my-4 text-subtitle-1">
                  10$ • La paz, Bolivia
                </div>

                <div>Sistema avanzado para rastrear, gestionar y optimizar inventario empresarial.</div>
              </v-card-text>

              <v-divider class="mx-4 mb-1"></v-divider>

              <v-card-actions>
                <v-btn color="deep-purple-lighten-2" text="Comprar" block border @click="reserve"></v-btn>
              </v-card-actions>
            </v-card>
          </v-col>

          <v-col cols="auto" class="card-col">
            <v-card :disabled="loading" :loading="loading" max-width="374">
              <template v-slot:loader="{ isActive }">
                <v-progress-linear :active="isActive" color="deep-purple" height="4" indeterminate></v-progress-linear>
              </template>

              <v-img height="250"
                src="public/el concepto del sistema de control de inventario, el gerente profesional y el trabajador están verificando el suministro de bienes y existencias, la gestión de inventario con la demanda de bienes.jpeg"
                cover></v-img>

              <v-card-item>
                <v-card-title>Plan Premium</v-card-title>

                <v-card-subtitle>
                  <span class="me-1">Nuevo</span>

                  <v-icon color="error" icon="mdi-fire-circle" size="small"></v-icon>
                </v-card-subtitle>
              </v-card-item>

              <v-card-text>
                <v-row align="center" class="mx-0">
                  <v-rating :model-value="4.8" color="amber" density="compact" size="small" half-increments
                    readonly></v-rating>

                  <div class="text-grey ms-4">
                    4.8 (530)
                  </div>
                </v-row>

                <div class="my-4 text-subtitle-1">
                  15$ • La paz, Bolivia
                </div>

                <div>Sistema premium para rastrear, gestionar y optimizar inventario empresarial con características adicionales.</div>
              </v-card-text>

              <v-divider class="mx-4 mb-1"></v-divider>

              <v-card-actions>
                <v-btn color="deep-purple-lighten-2" text="Comprar" block border @click="reserve"></v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </v-app>
</template>

<script>
import { useRouter } from 'vue-router'

export default {
  data: () => ({
    loading: false,
    selection: 1,
  }),

  setup() {
    const router = useRouter()

    const redirectTo = (path) => {
      router.push(path)
    }

    return {
      redirectTo,
      reserve() {
        this.loading = true
        setTimeout(() => (this.loading = false), 2000)
      },
    }
  },
}
</script>

<style scoped>
.fill-height {
  height: 100vh;
}
.andale-mono {
  font-family: 'Andale Mono', monospace;
}
.card-col {
  margin: 0 0.7rem;
}
</style>
