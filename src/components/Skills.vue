<template>
      <div class="s-page-container">
        <div class="s-title-container noir mx-auto mb-13">&lt;Skills&gt;</div>
            <div class="skills-container mx-auto mt-n6 mb-5">
                <skill-bubble lang-name="Java">
                    <v-icon size="40" color="white">mdi-language-java</v-icon>
                </skill-bubble>
                <skill-bubble lang-name="C#">
                    <v-icon size="40" color="white">mdi-language-csharp</v-icon>
                </skill-bubble>
                <skill-bubble lang-name="C">
                    <v-icon size="40" color="white">mdi-language-c</v-icon>
                </skill-bubble>
                <skill-bubble lang-name="Python">
                    <v-icon size="40" color="white">mdi-language-python</v-icon>
                </skill-bubble>
                <skill-bubble lang-name="JavaScript">
                    <v-icon size="40" color="white">mdi-language-javascript</v-icon>
                </skill-bubble>
                <skill-bubble lang-name="HTML">
                    <v-icon size="40" color="white">mdi-language-html5</v-icon>
                </skill-bubble>
                <skill-bubble lang-name="CSS">
                    <v-icon size="40" color="white">mdi-language-css3</v-icon>
                </skill-bubble>
                <skill-bubble lang-name="VueJS">
                    <v-icon size="40" color="white">mdi-vuejs</v-icon>
                </skill-bubble>
            </div>
                <div class="btn-container">
                    <v-btn 
                    @click=downloadCV
                    class="ma-2 mt-5"
                    outlined
                    color="#41B883"
                    >
                    Download my CV</v-btn>
            </div>
      </div>
</template>

<script>
import skillBubble from './skill-bubble.vue'
export default {
  components: { skillBubble },
  methods: {
      downloadCV () {
          window.open('https://drive.google.com/file/d/1SoSOM38J_q5d6fPDWopFHo-gYxx152kw/view?usp=sharing');
      }
  }
}
</script>

<style scoped>
.s-page-container {
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    justify-content: center;
    align-content: center;
    height: 60vh;
}
.skills-container {
    display: flex;
    align-content: center;
    justify-content: center;
    flex-direction: row;
    flex-wrap: wrap;
}
.s-title-container {
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    color: rgb(21, 22, 24);
}
.noir {
    font-family: 'Noir-regular';
    font-weight: bold;
    font-size: 40px;
}
.btn-container {
    display: flex;
    justify-content: center;
    align-content: center;
    flex-wrap: wrap;
}
a {
    text-decoration: none;
}
</style>