<template>
  <v-app>

    <v-main>
      <landing-page id="landing">
          <v-btn
            @click="scroll('skills')"
            slot="btn"
            class="mx-auto mt-n5"
            color= "white"
            icon
            >
            <v-icon>mdi-chevron-down</v-icon>
          </v-btn>
      </landing-page>
      <skills-page id="skills"></skills-page>
      <projects-page id="projects"></projects-page>
      <contact-page>
          <v-btn
            @click="scroll('landing')"
            slot="btn"
            class="mx-auto mt-n5 mb-5"
            color= "white"
            outlined
            >
            Back to top
          </v-btn>
      </contact-page>
    </v-main>
  </v-app>
</template>

<script>
import ContactPage from './components/contactPage.vue';
//import HelloWorld from './components/HelloWorld';
import LandingPage from './components/LandingPage.vue';
import ProjectsPage from './components/ProjectsPage.vue';
import SkillsPage from './components/Skills.vue';
export default {
  name: 'App',

  components: {
    //HelloWorld,
    LandingPage,
    ProjectsPage,
    SkillsPage,
    ContactPage,
  },
  data: () => ({
    //
  }),
  methods: {
    scroll(id) {  
      document.getElementById(id).scrollIntoView({
        behavior: "smooth"
      });
    }
  }
}
</script>

<style scoped>
@font-face {
  font-family: "Noir-medium";
  src: local("Noir-medium"),
   url(./assets/fonts/Noir_medium.otf) format("truetype");
  font-family: "Noir-regular";
  src: local("Noir-regular"),
   url(./assets/fonts/Noir_regular.otf) format("truetype");
}
.flex-item-p {
    flex-direction: column;
    justify-content: center;
    align-content: flex-start;
    color: white;
}
.font-family {
    font-family: 'Noir-regular';
    font-weight: bold;
}
</style>