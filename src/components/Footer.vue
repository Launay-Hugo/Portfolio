<script setup></script>

<template>
  <footer class="footer">
    <p>© 2024 Hugo Launay. Tous droits réservés.</p>
    <div class="social-links">
      <a href="https://github.com/Launay-Hugo">GitHub</a>
      <a href="https://www.linkedin.com/in/hugo-launay-b17b3426b/">LinkedIn</a>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background-color: #1e1e1e;
  color: #fff;
  padding: 20px;
  text-align: center;
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  box-shadow: 0 -2px 5px rgba(0, 0, 0, 0.2);
}

.footer .social-links a {
  margin: 0 10px;
  color: var(--green);
  text-decoration: none;
  font-weight: bold;
  transition: color 0.3s ease;
}

.footer .social-links a:hover {
  color: var(--lightgreen);
  text-decoration: underline;
}
</style>
