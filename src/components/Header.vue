<script setup>
import { ref } from 'vue'
const showModal = ref(false)
</script>
<template>
  <header class="header">
    <h1>Mon Portfolio</h1>
    <nav>
      <a href="#" @click.prevent="showModal = true">Contact</a>
    </nav>
    <div v-if="showModal" class="modal">
      <div class="modal-content">
        <h2>Contactez-moi</h2>
        <p>
          GitHub :
          <a href="https://github.com/Launay-Hugo" target="_blank"
            >https://github.com/Launay-Hugo</a
          >
        </p>
        <p>
          LinkedIn :
          <a href="https://linkedin.com/in/votre-profil" target="_blank"
            >www.linkedin.com/in/ hugo-launay-hg
          </a>
        </p>
        <p>Email : <a href="mailto:launay.hg@gmail.com">launay.hg@gmail.com</a></p>
        <button @click="showModal = false" class="close-button">OK</button>
      </div>
    </div>
  </header>
</template>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background: linear-gradient(45deg, var(--green), var(--lightgreen));
  color: #fff;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  font-size: 20px;
}

.header nav a {
  margin: 0 15px;
  color: #fff;
  text-decoration: none;
  font-weight: bold;
}
.header nav a:hover {
  color: var(--green);
  text-decoration: underline;
}

.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.modal-content {
  background: #fff;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
  text-align: center;
  width: 80%;
  max-width: 400px;
}

.modal-content h2 {
  color: black;
  margin-bottom: 10px;
}

.modal-content a {
  color: blue;
  text-decoration: none;
  margin-right: 40px;
}

.modal-content a:hover {
  text-decoration: underline;
}

.close-button {
  margin-top: 20px;
  padding: 10px 20px;
  background: var(--green);
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 16px;
}

.close-button:hover {
  background: var(--lightgreen);
}
</style>
