<script setup>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import ProjectListView from './views/ProjectListView.vue'
</script>

<template>
  <div id="app">
    <Header />
    <main class="content">
      <ProjectListView />
    </main>
    <Footer />
  </div>
</template>
<style scoped>
#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.content {
  flex: 1; /* Permet à la section principale de s'étendre */
  padding: 30px;
  background-color: #f4f4f9;
  padding-bottom: 100px;
}
</style>
