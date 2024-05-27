<template>
  <div class="content">
    <div class="text-center">
      <h1 :style="{ fontSize: textSize + 'px' }" class="titulo">Nuestro sistema de inventarios</h1>
      <p class="descripcion">Gestiona y controla productos, optimizando niveles de stock eficientemente.</p>
      <button class="prueba-btn" @click="pruebaGratis">¡Pruébalo gratis!</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      textSize: 70 // Tamaño de texto inicial
    };
  },
  methods: {
    pruebaGratis() {
      // Acción al hacer clic en el botón "¡Pruébalo gratis!"
      // Aquí puedes agregar la lógica para redirigir al usuario a una página de prueba gratuita o abrir un formulario de registro
      console.log('Botón de prueba gratis clickeado');
    }
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Caveat&display=swap');

.content {
  display: flex;
  justify-content: center; /* Centra horizontalmente */
  align-items: center; /* Centra verticalmente */
  height: 80vh; /* Opcional: ajusta la altura según tus necesidades */
}

.text-center {
  text-align: center;
}

.titulo {
  font-family: 'Caveat', cursive; /* Utilizamos 'Caveat' como la fuente principal */
  margin: 0; /* Elimina el margen superior e inferior */
}

.descripcion {
  font-size: 24px; /* Tamaño de texto para la descripción */
  margin-top: 20px; /* Espacio entre el título y la descripción */
  font-family: 'Caveat', cursive;
}

.prueba-btn {
  margin-top: 20px; /* Espacio entre la descripción y el botón */
  font-size: 18px; /* Tamaño de texto del botón */
  padding: 10px 20px;
  color: white; /* Color del texto del botón */
  background-color: #d29cf9; /* Color de fondo del botón (igual que el app bar) */
  border: none; /* Sin borde */
  border-radius: 4px; /* Bordes redondeados */
  cursor: pointer; /* Cursor de mano al pasar sobre el botón */
  transition: background-color 0.3s ease; /* Transición suave para el color de fondo */
}

.prueba-btn:hover {
  background-color: #d6baf8; /* Color de fondo al pasar el mouse (más oscuro) */
}
</style>
