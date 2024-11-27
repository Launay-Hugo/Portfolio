<script setup>
defineProps({
  title: String,
  description: String,
  image: String,
  link: String,
  git: String,
})
</script>

<template>
  <div class="project-card">
    <img :src="image" :alt="title" />
    <h3>{{ title }}</h3>
    <p>{{ description }}</p>
    <a :href="git" target="_blank">Lien vers Git</a>
    <a :href="link" target="_blank">Voir le projet</a>
  </div>
</template>

<style scoped>
.project-card {
  background: white;
  border: 1px solid #ddd;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition:
    transform 0.3s ease,
    box-shadow 0.3s ease;
  width: 100%;
  max-width: 300px;
  margin: 0 auto;
}

.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

.project-card img {
  width: 80%;
  height: 200px;
  object-fit: cover;
  margin-top: 20px;
}

.project-card h3 {
  font-size: 20px;
  margin: 15px 0;
  color: #333;
}

.project-card p {
  color: #555;
  font-size: 14px;
  margin: 10px 20px;
}

.project-card a {
  display: inline-block;
  margin: 10px 20px;
  padding: 10px 15px;
  background-color: var(--green);
  color: white;
  text-decoration: none;
  border-radius: 5px;
  font-weight: bold;
  transition: background-color 0.3s ease;
}

.project-card a:hover {
  background-color: var(--lightgreen);
}
@media (max-width: 768px) {
  .project-card {
    margin: 0 auto; /* Centrer les cards */
  }
}
</style>
