<template>
  <section id="testimonials" class="testimonials">
    <div class="container">
      <h2>Lo que dicen nuestros clientes</h2>
      <div class="testimonials-grid">
        <div class="testimonial-card" v-for="(testimonial, index) in testimonials" :key="index">
          <div class="quote-icon">“</div>
          <p class="comment">{{ testimonial.comment }}</p>
          <div class="author">
            <div class="author-avatar">
              <span>{{ testimonial.initials }}</span>
            </div>
            <div class="author-info">
              <h4>{{ testimonial.name }}</h4>
              <span>{{ testimonial.role }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const testimonials = [
  {
    comment: "Gracias al equipo de Estudio Contable, logramos ordenar nuestras finanzas y optimizar nuestra carga tributaria. Su profesionalismo es impecable.",
    name: "Carlos Rodríguez",
    role: "CEO de TechSolutions",
    initials: "CR"
  },
  {
    comment: "La atención personalizada que brindan es lo que los diferencia. Siempre están disponibles para resolver mis dudas con claridad y rapidez.",
    name: "Mariana López",
    role: "Dueña de Café Central",
    initials: "ML"
  },
  {
    comment: "Excelentes profesionales. Nos han acompañado en el crecimiento de nuestra empresa desde el primer día con asesoramiento estratégico.",
    name: "Julián Méndez",
    role: "Director de Inmobiliaria Méndez",
    initials: "JM"
  }
];
</script>

<style scoped src="../styles/testimonials.css"></style>
