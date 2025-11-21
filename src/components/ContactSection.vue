<template>
  <section id="contact" class="contact">
    <div class="container">
      <h2>Contáctenos</h2>
      <div class="contact-wrapper">
        <div class="contact-info">
          <h3>Estamos para ayudarlo</h3>
          <p>Complete el formulario o utilice nuestros canales directos de comunicación.</p>
          
          <div class="info-item">
            <div class="icon">📍</div>
            <div>
              <h4>Ubicación</h4>
              <p>Av. Corrientes 1234, Buenos Aires</p>
            </div>
          </div>
          
          <div class="info-item">
            <div class="icon">📞</div>
            <div>
              <h4>Teléfono</h4>
              <p>+54 11 1234-5678</p>
            </div>
          </div>
          
          <div class="info-item">
            <div class="icon">✉️</div>
            <div>
              <h4>Email</h4>
              <p>info@estudiocontable.com</p>
            </div>
          </div>
        </div>

        <form class="contact-form" @submit.prevent="handleSubmit">
          <div class="form-group">
            <label for="name">Nombre Completo</label>
            <input type="text" id="name" v-model="form.name" required placeholder="Su nombre">
          </div>
          
          <div class="form-group">
            <label for="email">Email</label>
            <input type="email" id="email" v-model="form.email" required placeholder="nombre@ejemplo.com">
          </div>
          
          <div class="form-group">
            <label for="subject">Asunto</label>
            <select id="subject" v-model="form.subject">
              <option value="Consulta General">Consulta General</option>
              <option value="Liquidación de Impuestos">Liquidación de Impuestos</option>
              <option value="Balances">Balances</option>
              <option value="Asesoría">Asesoría</option>
            </select>
          </div>
          
          <div class="form-group">
            <label for="message">Mensaje</label>
            <textarea id="message" v-model="form.message" rows="5" required placeholder="¿En qué podemos ayudarlo?"></textarea>
          </div>
          
          <button type="submit" class="btn btn-block">Enviar Mensaje</button>
        </form>
      </div>
    </div>
  </section>
</template>

<script setup>
import { reactive } from 'vue';

const form = reactive({
  name: '',
  email: '',
  subject: 'Consulta General',
  message: ''
});

const handleSubmit = () => {
  alert(`Gracias ${form.name}, hemos recibido su consulta. Nos pondremos en contacto pronto.`);
  // Reset form logic here
  form.name = '';
  form.email = '';
  form.message = '';
};
</script>

<style scoped src="../styles/contact.css"></style>
