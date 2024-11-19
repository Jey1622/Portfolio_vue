<template>
  <v-app>
    <v-app-bar app>
      <v-toolbar-title>My portfolio</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text @click="scrollToSection('intro')" class="btn">Intro</v-btn>
      <v-btn text @click="scrollToSection('about')" class="btn">About Me</v-btn>
      <v-btn text @click="scrollToSection('resume')" class="btn">Resume</v-btn>
      <v-btn text @click="scrollToSection('contact')" class="btn">contact</v-btn>
    </v-app-bar>
    <v-main>
      <v-container>
        <div id="intro">
          <intro />
        </div>
        <div id="about">
          <about />
        </div>
        <div id="resume">
          <resume />
        </div>
        <div id="contact">
          <contact />
        </div>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import About from "./components/About.vue";
import Contact from "./components/Contact.vue";
import Intro from "./components/Intro.vue";
import Resume from "./components/Resume.vue";

export default {
  name: "App",

  components: {
    Intro,
    About,
    Resume,
    Contact,
  
  },
  methods: {
    scrollToSection(sectionId) {
      const section = document.getElementById(sectionId);
      section.scrollIntoView({ behavior: "smooth" });
    },
    
  },

  data(){
    
  },
};
</script>
<style>
#intro,
#about,
#resume,
#contact {
  margin: 40px 0;
}
.btn {
  background-color: #00ea85;
  color: #ffffff;
  transition: background-color 0.3s, color 0.3s;
  margin: 10px;
}
.btn:hover {
  background-color: #00ea85;
  color: #ffffff;
}
</style>
