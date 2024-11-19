<template>
    <v-container class="pa-5">
      <v-row align="center" justify="center">
        <v-col cols="12" md="8">
          <div class="about-container">
            <v-row no-gutters>
              <v-col cols="12" md="4" class="d-flex align-center justify-center">
                <v-avatar size="200" class="mb-4">
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
                <h1 class="headline">About Me</h1>
                <p>Hello! I'm Jeyaraman S, a dedicated and passionate web developer with a strong background in MERN. I have a knack for turning complex problems into simple, beautiful solutions. I enjoy working on innovative projects and am always eager to learn new things and take on new challenges.</p>
                <ul class="details-list">
                    <li><strong>Degree:</strong> Bachelor of Electronics and communication Engineering</li>
                  <li><strong>Date of Birth:</strong> 22 April 2003</li>
                  <li><strong>Age:</strong> 21</li>
                  <li><strong>Phone Number:</strong> +91 9384121622</li>
                  <li><strong>Email ID:</strong> jeyaramanapr22@gmail.com</li>
                  <li><strong>City:</strong> Virudhunagar,TamilNadu,India</li>
                </ul>
              </v-col>
            </v-row>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  export default {
    name: 'AboutSection',
  };
  </script>
  
  <style scoped>
  .about-container {
    padding: 20px;
    /* background-color: #f9f9f9; */
    border-radius: 8px;
  }
  
  .headline {
    font-size: 28px;
    font-weight: bold;
    margin-bottom: 15px;
  }
  
  .details-list {
    list-style-type: none;
    padding: 0;
    margin-top: 20px;
  }
  
  .details-list li {
    margin-bottom: 10px;
  }
  .full-image img {
  object-fit: contain;
}
  </style>
  