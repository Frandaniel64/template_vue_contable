<template>
  <section id="services" class="services">
    <div class="container">
      <h2>Nuestros Servicios</h2>
      <div class="services-grid">
        <div class="service-card" v-for="(service, index) in services" :key="index">
          <div class="icon-box">{{ service.icon }}</div>
          <h3>{{ service.title }}</h3>
          <p>{{ service.description }}</p>
          <a href="#contact" class="learn-more">Consultar &rarr;</a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const services = [
  {
    title: 'Liquidación Impositiva',
    description: 'Gestión completa de impuestos nacionales, provinciales y municipales. DDJJ mensuales y anuales.',
    icon: '📝'
  },
  {
    title: 'Balances',
    description: 'Elaboración y certificación de estados contables. Auditorías y presentación ante organismos de control.',
    icon: '📊'
  },
  {
    title: 'Asesorías',
    description: 'Consultoría permanente para la toma de decisiones estratégicas en su negocio o emprendimiento.',
    icon: '🤝'
  },
  {
    title: 'Planificación Impositiva',
    description: 'Análisis y proyección fiscal para optimizar la carga tributaria de manera legal y eficiente.',
    icon: '💡'
  }
];
</script>

<style scoped src="../styles/services.css"></style>
