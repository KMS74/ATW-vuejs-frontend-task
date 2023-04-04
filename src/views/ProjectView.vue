<template>
  <h1 class="heading-primary">Our <br />Projects</h1>
  <!-- Tabbed Projects Section -->
  <TabsContainer>
    <TabItem name="Web Design" :selected="true">
      <div class="recent-projects">
        <ProjectCard v-for="project of projects" :key="project.title" :title="project.title"
          :imagePath="project.imagePath" />
      </div>
    </TabItem>
    <TabItem name="Mobile App Design">
      <!-- we shuffled the projects array to simulte displaying diffrent content inside each TabItem -->
      <div class="recent-projects">
        <ProjectCard v-for="project of shuffledArr(projects)" :key="project.title" :title="project.title"
          :imagePath="project.imagePath" />
      </div>
    </TabItem>
    <TabItem name="Freebies">
      <div class="recent-projects">
        <ProjectCard v-for="project of shuffledArr(projects)" :key="project.title" :title="project.title"
          :imagePath="project.imagePath" />
      </div>
    </TabItem>
  </TabsContainer>
  <!-- Email CTA -->
  <EmailCTA />
  <!-- Footer -->
  <TheFooter />
</template>

<script>
import ProjectCard from '../components/ProjectCard.vue'
import TabItem from '../components/TabItem.vue'
import TabsContainer from '../components/TabsContainer.vue'
import EmailCTA from '../components/EmailCTA.vue'
import TheFooter from '../components/TheFooter.vue'
import portofolioImage from "../assets/images/portofolio.jpg"
import lummyImage from "../assets/images/lummy.jpg"
import keeperImage from "../assets/images/keeper.jpg"
import planImage from "../assets/images/plans-g187d0953c_640.jpg"




export default {

  data() {
    return {
      projects: [
        {
          title: 'Ant - Personal Portofolio',
          imagePath: portofolioImage
        },
        {
          title: 'Lumy - Dashboard UI Kit',
          imagePath: lummyImage
        },
        {
          title: 'Keeper - Soccer Site',
          imagePath: keeperImage
        },
        {
          title: 'Minify - Web Design',
          imagePath: planImage
        }
      ]
    }
  },
  methods: {
    // suffle array method
    shuffledArr(array) {
      return array.sort(() => 0.5 - Math.random())
    }
  },
  components: { TabsContainer, TabItem, ProjectCard, EmailCTA, TheFooter }
}
</script>

<style scoped>
.recent-projects {
  display: grid;
  grid-template-columns: 1fr 1fr;
  column-gap: 3rem;
  row-gap: 8rem;
  margin-bottom: 15rem;
}

@media (max-width: 600px) {
  .recent-projects {
    grid-template-columns: 1fr;
    row-gap: 4rem;
  }
}
</style>
