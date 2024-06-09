<template>
  <div class="content" :style="contentStyle">
    <div class="text-center">
      <h1 :style="{ fontSize: textSize + 'px' }" class="titulo">Nuestro sistema de inventarios</h1>
      <p class="descripcion">Gestiona y controla productos, optimizando niveles de stock eficientemente.</p><br>
      <button class="prueba-btn" @click="pruebaGratis">¡Pruébalo ahora!</button>
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
      this.$router.push('/products');
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
  background-image: url('https://images.unsplash.com/photo-1557682250-33bd709cbe85?q=80&w=1000&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxleHBsb3JlLWZlZWF8MXx8fGVufDB8fHx8fA%3D%3D');
  background-size: cover; /* Ajusta la imagen para que cubra todo el fondo */
  background-position: center; /* Centra la imagen de fondo */
  background-repeat: no-repeat; /* Evita que la imagen se repita */
}

.text-center {
  text-align: center;
  background-color: rgba(255, 255, 255, 0.8); /* Fondo semitransparente para mejorar la legibilidad del texto */
  padding: 20px;
  border-radius: 10px;
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
</style>
