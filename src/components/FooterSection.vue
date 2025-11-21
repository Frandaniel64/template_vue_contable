<template>
  <footer class="footer">
    <div class="container footer-content">
      <div class="footer-logo">
        <span class="logo-text">Estudio<span class="highlight">Contable</span></span>
        <p>Excelencia y compromiso en servicios contables.</p>
      </div>
      
      <div class="footer-links">
        <h4>Enlaces Rápidos</h4>
        <ul>
          <li><a href="#home">Inicio</a></li>
          <li><a href="#about">Quiénes Somos</a></li>
          <li><a href="#services">Servicios</a></li>
          <li><a href="#contact">Contacto</a></li>
        </ul>
      </div>
      
      <div class="footer-social">
        <h4>Síguenos</h4>
        <div class="social-icons">
          <a href="#" aria-label="Facebook">FB</a>
          <a href="#" aria-label="LinkedIn">IN</a>
          <a href="#" aria-label="Instagram">IG</a>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <p>&copy; {{ new Date().getFullYear() }} Estudio Contable. Todos los derechos reservados.</p>
    </div>
  </footer>
</template>

<style scoped src="../styles/footer.css"></style>
