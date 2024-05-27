<template>
  <div class="content" :style="contentStyle">
    <div class="text-center">
      <h1 :style="{ fontSize: textSize + 'px' }" class="titulo">Nuestro sistema de inventarios</h1>
      <p class="descripcion">Gestiona y controla productos, optimizando niveles de stock eficientemente.</p>
      <button class="prueba-btn" @click="pruebaGratis">¡Pruébalo gratis!</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    textSize: {
      type: Number,
      default: 70
    },
    marginTop: {
      type: String,
      default: '0px'
    },
    marginBottom: {
      type: String,
      default: '-60px'
    }
  },
  computed: {
    contentStyle() {
      return {
        marginTop: this.marginTop,
        marginBottom: this.marginBottom
      };
    }
  },
  methods: {
    pruebaGratis() {
      console.log('Botón de prueba gratis clickeado');
    }
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Caveat&display=swap');

.content {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 80vh; /* Ajusta la altura según tus necesidades */
}

.text-center {
  text-align: center;
}

.titulo {
  font-family: 'Caveat', cursive;
  margin: 0;
}

.descripcion {
  font-size: 24px;
  margin-top: 20px; /* Espacio entre el título y la descripción */
  font-family: 'Caveat', cursive;
}

.prueba-btn {
  margin-top: 10px; /* Espacio entre la descripción y el botón */
  font-size: 18px;
  padding: 10px 20px;
  color: white;
  background-color: #d29cf9;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.prueba-btn:hover {
  background-color: #d6baf8;
}
</style>
