<script setup>
import ProjectCard from '@/components/ProjectCard.vue'

const projects = [
  {
    id: 1,
    title: 'Projet 1',
    description: 'Reproduction du site LeBonCoin fait avec LeReacteur',
    image: 'https://res.cloudinary.com/dskfvpsiu/image/upload/v1732552181/ExoLBC_qdfuue.png',
    git: 'https://github.com/Launay-Hugo/ExoLBC',
    link: 'https://exolbc.netlify.app',
  },
  {
    id: 2,
    title: 'Projet 2',
    description: 'HTLM/CSS Reproduction du site EasyJett',
    image: 'https://res.cloudinary.com/dskfvpsiu/image/upload/v1732610595/easyjet_ds67fi.png',
    git: 'https://github.com/Launay-Hugo/easyJet.git',
    link: 'https://easyjetcss.netlify.app/',
  },
  {
    id: 3,
    title: 'Projet 3',
    description: 'Premier Projet Perso (V1) lors de la formation',
    image:
      'https://res.cloudinary.com/dskfvpsiu/image/upload/v1732552666/PremierProjetv1_kqbty9.png',
    git: 'https://github.com/Launay-Hugo/ProjetFitness',
    link: 'https://projetfitness.netlify.app/',
  },
  {
    id: 4,
    title: 'Projet 4',
    description: 'Projet Perso Remasterisé (V2) a la fin de la formation',
    image: 'https://res.cloudinary.com/dskfvpsiu/image/upload/v1732552605/ProjetPerso_yhivo7.png',
    git: 'https://github.com/Launay-Hugo/ProjetPersoV2',
    link: 'https://projetfitnessv2.netlify.app/',
  },
]
</script>

<template>
  <section id="projects" class="project-list">
    <h2>Mes Projets</h2>
    <div class="projects-grid">
      <ProjectCard
        v-for="project in projects"
        :key="project.id"
        :title="project.title"
        :description="project.description"
        :image="project.image"
        :link="project.link"
        :git="project.git"
      />
    </div>
  </section>
</template>

<style scoped>
.project-list {
  text-align: center;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva,
    Verdana, sans-serif;
}
.project-list h2 {
  font-weight: bold;
  font-size: 24px;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr); /* 3 colonnes */
  gap: 20px;
  padding-top: 24px;
  margin-left: 140px;
  margin-right: 140px;
  justify-content: center; /* Centre les projets horizontalement */
}

.projects-grid > :nth-child(4) {
  grid-column: 2 / 3; /* Centre le 4ème projet */
}
@media (max-width: 768px) {
  .projects-grid {
    grid-template-columns: 1fr; /* Single column on small screens */
  }
}
</style>
