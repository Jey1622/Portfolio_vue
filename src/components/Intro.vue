<template>
  <v-container class="pa-5">
    <v-row align="center" justify="center">
      <v-col cols="12" md="8">
        <v-card class="flat-card">
          <v-row no-gutters>
            <v-col cols="12" md="4" class="d-flex align-center justify-center">
              <v-avatar size="200" class="mt-5">
                <img
                  :src="require('@/assets/Images/1.jpg')"
                  alt="Profile pictre"
                  contain
                  class="full-image"
                  max-width="100%"
                  height="200px"
                />
              </v-avatar>
            </v-col>
            <v-col cols="12" md="8">
              <v-card-title class="headline">Hi, I'm JEYARAMAN</v-card-title>
              <v-card-text>
                <p>
                  I am a dedicated and passionate web developer with a love for
                  creating innovative and efficient web applications. With a
                  strong foundation in Vue JS , I enjoy solving complex problems
                  and turning ideas into reality.
                </p>
                <v-btn color="primary" class="mt-4" @click="downloadResume"
                  >Download Resume</v-btn
                >
                <v-btn
                  outlined
                  color="secondary"
                  class="mt-4 ml-2"
                  @click="contactMe"
                  >Contact Me</v-btn
                >
              </v-card-text>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>
  
  <script>
export default {
  name: "IntroSection",
  methods: {
    downloadResume() {
      // Logic to download the resume
      const link = document.createElement("a");
      link.href =
        "https://drive.google.com/file/d/16LGtfloazlM0Kwu9GXliZ3mwNeG9e8dN/view?usp=drivesdk";
      link.download = "Resume.pdf";
      link.click();
    },
    contactMe() {
      // Logic to scroll to the contact section
      const section = document.getElementById("contact");
      section.scrollIntoView({ behavior: "smooth" });
    },
  },
};
</script>
  
  <style scoped>
.flat-card {
  box-shadow: none;
  border: none;
}

.headline {
  font-size: 28px;
  font-weight: bold;
}
.full-image img {
  object-fit: contain;
}
</style>
  