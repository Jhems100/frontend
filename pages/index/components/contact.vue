<template>
  <v-main>
    <v-container class="contact-container" fluid>
      <v-row align="center" justify="space-between">
        <v-col cols="12" sm="6">
          <div class="text-content">
            <h1 class="headline">Contáctanos</h1>
            <p>¡Estamos aquí para ayudarte! Puedes ponerte en contacto con nosotros a través del siguiente formulario o aproximese a nuestras oficinas:</p>
            <form @submit.prevent="submitForm">
              <div class="form-group">
                <label for="name">Nombre:</label>
                <input type="text" id="name" v-model="formData.name" required>
              </div>
              <div class="form-group">
                <label for="email">Correo Electrónico:</label>
                <input type="email" id="email" v-model="formData.email" required>
              </div>
              <div class="form-group">
                <label for="phone">Teléfono:</label>
                <input type="tel" id="phone" v-model="formData.phone" required>
              </div>
              <div class="form-group">
                <label for="message">Mensaje:</label>
                <textarea id="message" v-model="formData.message" rows="4" required></textarea>
              </div>
              <button type="submit">Enviar</button>
            </form>
          </div>
        </v-col>
        <v-col cols="12" sm="6">
          <!-- Embed de Google Maps con la ubicación de La Paz, Bolivia -->
          <iframe
            width="100%"
            height="400"
            frameborder="0"
            style="border:0"
            allowfullscreen=""
            loading="lazy"
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d195799.87415950923!2d-68.2064415993096!3d-16.507133816379868!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x916cd19f76b6777d%3A0x1001b8452ba4250!2sLa%20Paz%2C%20Bolivia!5e0!3m2!1sen!2sus!4v1635960089710!5m2!1sen!2sus"
          ></iframe>
        </v-col>
      </v-row>
    </v-container>
  </v-main>
</template>

<script>
export default {
  name: 'Contact',
  data() {
    return {
      formData: {
        name: '',
        email: '',
        phone: '',
        message: ''
      }
    };
  },
  methods: {
    submitForm() {
      // Aquí puedes implementar la lógica para enviar el formulario
      console.log('Formulario enviado:', this.formData);
      // Puedes resetear el formulario después de enviarlo si lo deseas
      this.formData = {
        name: '',
        email: '',
        phone: '',
        message: ''
      };
    }
  }
}
</script>

<style scoped>
.contact-container {
  padding: 50px 20px;
}

.text-content {
  max-width: 600px;
  font-family: 'Noto Sans', sans-serif;
}

.headline {
  color: #000000;
  font-weight: 700;
  margin-bottom: 20px;
  font-size: 2.5rem;
}

.form-group {
  margin-bottom: 20px;
}

label {
  color: #000000;
  display: block;
  font-weight: bold;
}

input[type="text"],
input[type="email"],
input[type="tel"],
textarea {
  width: 100%;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

button {
  padding: 10px 20px;
  background-color: #8c7ae6;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #826deb;
}

iframe {
  width: 100%;
  height: 400px;
  border: none;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

iframe:hover {
  transform: translateY(-5px);
}
</style>
