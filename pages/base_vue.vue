<template>
  <div class="container">
    <div class="product-card">
      <h2 class="product-title">Nombre del Producto</h2>
      <p class="product-description">Descripción del Producto</p>
      <p class="product-price">$19.99</p>
    </div>
  </div>
</template>

<script>
export default {
  // Componente Vue.js
};
</script>

<style scoped>
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

.product-card {
  background-color: #f8f8f8;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: 20px;
}

.product-title {
  font-size: 1.5em;
  font-weight: bold;
  color: #333;
}

.product-description {
  font-size: 1.1em;
  color: #666;
  margin-top: 10px;
}

.product-price {
  font-size: 1.2em;
  font-weight: bold;
  color: #007bff;
  margin-top: 10px;
}
</style>
