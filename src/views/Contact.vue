<template>
  <div class="container mt-5">
    <h2 class="text-primary fw-bold mb-4">Contacto</h2>
    
    <p class="text-gray-300 fs-5 mb-2">
      📞 Teléfono: <a href="tel:+525567463024">5567463024</a>
    </p>
    <p class="text-gray-300 fs-5 mb-2">
      📧 Correo: <a href="mailto:adrianguma99@gmail.com">adrianguma99@gmail.com</a>
    </p>
    <p class="text-gray-300 fs-5 mb-4">
      🔗 LinkedIn: <a href="https://www.linkedin.com/in/adriang-guzman" target="_blank">adriang-guzman</a>
    </p>

    <h3 class="text-primary fw-bold mb-3">O envíame un mensaje</h3>
    <form @submit.prevent="sendEmail" ref="form">
      <div class="mb-3">
        <input type="text" class="form-control" placeholder="Nombre" v-model="name" required>
      </div>
      <div class="mb-3">
        <input type="email" class="form-control" placeholder="Correo electrónico" v-model="email" required>
      </div>
      <div class="mb-3">
        <textarea class="form-control" rows="4" placeholder="Mensaje" v-model="message" required></textarea>
      </div>
      <button type="submit" class="btn btn-primary">Enviar</button>
    </form>
    <p v-if="statusMessage" class="mt-3">{{ statusMessage }}</p>
  </div>
</template>

<script>
import emailjs from 'emailjs-com';

export default {
  data() {
    return {
      name: '',
      email: '',
      message: '',
      statusMessage: ''
    }
  },
  methods: {
    sendEmail() {
      const serviceID = 'service_mwucc9x';
      const templateID = 'template_ejpnlrq';
      const userID = 'PRFHujFAyOJzSqnJv';

      emailjs.send(serviceID, templateID, {
        from_name: this.name,
        from_email: this.email,
        message: this.message
      }, userID)
      .then(() => {
        this.statusMessage = '¡Mensaje enviado con éxito! ✅';
        this.name = '';
        this.email = '';
        this.message = '';
      }, (err) => {
        this.statusMessage = 'Error al enviar el mensaje 😢';
        console.error(err);
      });
    }
  }
}
</script>