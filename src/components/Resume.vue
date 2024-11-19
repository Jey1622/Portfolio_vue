<template>
  <v-container class="pa-5">
    <v-row align="center" justify="center">
      <v-col cols="12" md="10">
        <h1 class="headline">Resume</h1>

        <!-- Work Experience Section -->
        <h2 class="subheadline">Work Experience</h2>
        <v-list>
          <v-list-item
            v-for="(experience, index) in workExperience"
            :key="index"
          >
            <v-list-item-content>
              <v-list-item-title>{{ experience.position }}</v-list-item-title>
              <v-list-item-subtitle
                >{{ experience.company }} -
                {{ experience.duration }}</v-list-item-subtitle
              >
              <v-list-item-text>{{ experience.description }}</v-list-item-text>
            </v-list-item-content>
          </v-list-item>
        </v-list>

        <!-- Education Section -->
        <h2 class="subheadline">Education</h2>
        <v-list>
          <v-list-item
            v-for="(education, index) in educationHistory"
            :key="index"
          >
            <v-list-item-content>
              <v-list-item-title>{{ education.degree }}</v-list-item-title>
              <v-list-item-subtitle
                >{{ education.institution }} -
                {{ education.duration }}</v-list-item-subtitle
              >
              <v-list-item-text>{{ education.description }}</v-list-item-text>
            </v-list-item-content>
          </v-list-item>
        </v-list>

        <!-- Skills Section -->
        <h2 class="subheadline">Skills</h2>
        <v-container>
          <v-row>
            <v-col cols="12" md="6">
              <v-list>
                <v-list-item
                  v-for="(skill, index) in firstColumnSkills"
                  :key="index"
                >
                  <v-list-item-content>
                    <v-list-item-title>{{ skill.name }}</v-list-item-title>
                    <v-progress-linear
                      :value="skill.percentage"
                      color="primary"
                      height="8"
                      class="mt-2"
                    ></v-progress-linear>
                  </v-list-item-content>
                </v-list-item>
              </v-list>
            </v-col>
            <v-col cols="12" md="6">
              <v-list>
                <v-list-item
                  v-for="(skill, index) in secondColumnSkills"
                  :key="index + firstColumnSkills.length"
                >
                  <v-list-item-content>
                    <v-list-item-title>{{ skill.name }}</v-list-item-title>
                    <v-progress-linear
                      :value="skill.percentage"
                      color="primary"
                      height="8"
                      class="mt-2"
                    ></v-progress-linear>
                  </v-list-item-content>
                </v-list-item>
              </v-list>
            </v-col>
          </v-row>
        </v-container>

        <!-- Projects Section -->
        <h2 class="subheadline">Projects</h2>
        <v-list>
          <v-list-item v-for="(project, index) in projects" :key="index">
            <v-list-item-content>
              <v-list-item-title>{{ project.title }}</v-list-item-title>
              <v-list-item-subtitle>{{
                project.duration
              }}</v-list-item-subtitle>
              <v-list-item-text>{{ project.description }}</v-list-item-text>
              <v-chip-group column>
                <v-chip
                  v-for="(tech, techIndex) in project.technologies"
                  :key="techIndex"
                  >{{ tech }}</v-chip
                >
              </v-chip-group>
            </v-list-item-content>
          </v-list-item>
        </v-list>

        <!-- Certifications Section -->
        <h2 class="subheadline">Certifications</h2>
        <v-list>
          <v-list-item
            v-for="(certification, index) in certifications"
            :key="index"
          >
            <v-list-item-content>
              <v-list-item-title>{{ certification.name }}</v-list-item-title>
              <v-list-item-subtitle
                >{{ certification.institution }} -
                {{ certification.date }}</v-list-item-subtitle
              >
              <v-list-item-text>{{
                certification.description
              }}</v-list-item-text>
            </v-list-item-content>
          </v-list-item>
        </v-list>

        <!-- Extracurricular Activities Section -->
        <h2 class="subheadline">Extracurricular Activities</h2>
        <v-list>
          <v-list-item
            v-for="(activity, index) in extracurriculars"
            :key="index"
          >
            <v-list-item-content>
              <v-list-item-title>{{ activity.name }}</v-list-item-title>
              <v-list-item-subtitle>{{
                activity.duration
              }}</v-list-item-subtitle>
              <v-list-item-text>{{ activity.description }}</v-list-item-text>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-col>
    </v-row>
  </v-container>
</template>
  
  <script>
export default {
  name: "ResumeSection",
  data() {
    return {
      workExperience: [
        {
          position: "Intern",
          company: "Sutherland Global Service",
          duration: "Nov 2024 - Present",
          description:
            "Developing innovative web applications using modern frameworks.",
        },
      ],
      educationHistory: [
        {
          degree: "Bachelor of Electronics and Communication",
          institution: "Anna University",
          duration: "2020 - 2024",
          description:
            "Graduated with honors, focused on software development and algorithms.",
        },
        {
          degree: "HSLC",
          institution:
            "Government Higher Secondary School,Sankaralingapuram,Virudhunagar.",
          duration: "2018 - 2020",
          description:
            "I'm completed HSLC with 74.8%.I'm studied Computer Maths Group in HSLC",
        },
        {
          degree: "SSLC",
          institution:
            "Government Higher Secondary School,Sankaralingapuram,Virudhunagar.",
          duration: "2016 - 2018",
          description: "I'm completed sSLC with 86.6%.",
        },
      ],
      skills: [
        { name: "HTML/CSS", percentage: 95 },
        { name: "JavaScript", percentage: 90 },
        { name: "React", percentage: 85 },
        { name: "Redux", percentage: 55 },
        { name: "Vue.js", percentage: 85 },
        { name: "Vuetify", percentage: 80 },
        { name: "Node.js", percentage: 70 },
        { name: "Express.js", percentage: 80 },
        { name: "MongoDB", percentage: 80 },
        { name: "MySQL", percentage: 70 },
        { name: "PostgreSQL", percentage: 50 },
        { name: "Python", percentage: 75 },
        { name: "Java", percentage: 70 },
        { name: "c", percentage: 80 },
      ],
      projects: [
        {
          title: "Authentication TODO list web App",
          duration: "Oct 2024",
          description:
            "This project involves creating a full-stack web application with authentication and CRUD (Create, Read, Update, Delete) functionality for managing a TODO list. Users can register, log in, add tasks, edit tasks, mark them as completed, and delete tasks. The app ensures data security and user privacy by implementing proper authentication and authorization mechanisms.",
          technologies: ["React.js", "Node.js", "Express.js", "MongoDB"],
        },
        {
          title: "E-commerce website",
          duration: "Nov 2024",
          description:
            "An e-commerce platform with payment integration and user management.",
          technologies: ["React", "Redux", "Express", "MongoDB"],
        },
      ],
      certifications: [
        {
          name: "Internet of Things",
          institution: "NPTEL",
          date: "Feb 2022",
          description:
            "Acqired Knowledge in IOT concepts inncluding sensor networks,data communication,architecture.",
        },
        {
          name: "HTML,CSS,JavaScript for web Developer",
          institution: "Johns Hopkins University",
          date: "Aug 2023",
          description:
            " Completed a comprehensive course covering HTML, CSS, and JavaScript fundamentals through Johns Hopkins University on Coursera,earning a certification with a grade of 94 %.",
        },
        {
          name: " Programming with javaScript",
          institution: "Meta",
          date: "Sept 2023",
          description:
            " Successfully completed a JavaScript programming course provided by Meta on Coursera, covering advanced concepts in JavaScript development with a grade of 98 %.",
        },
        {
          name: " Introduction to Databases for Back-End Develepment",
          institution: "Meta",
          date: "Nov 2023",
          description:
            " Completed a course on databases essential for back-end development with a grade of 86 %, provided by Meta on Coursera.",
        },
        {
          name: " Java Programming: Solving Problems with Software",
          institution: "Duke University",
          date: "Jul 2024",
          description:
            " Attained a 96% in the Java Programming: Solving Problems with Software course, delivered by Duke University on Coursera.",
        },
        {
          name: " Object Oriented Programming in Java",
          institution: " University of california San Diego",
          date: "Aug 2023",
          description:
            " Earned 100% in the Object-Oriented Programming in Java course, provided by the University of California, San Diego on Coursera.",
        },
        {
          name: " Data Structures and Performance",
          institution: " University of california San Diego",
          date: "Aug 2023",
          description:
            " Achieved a 94% in the Data Structures and Performance course, offered by the University of San Diego on Coursera.",
        },
      ],
      extracurriculars: [
        {
          name: "Nactional Service Scheme(NSS) Volunteer",
          duration: "Sep 2020 - May 2020",
          description:
            "Actively participate in community service and social initiatives as an NSS volunteer at UCE-BIT Campus, contributing to various projects aimed at societal welfare and development.",
        },
        {
          name: "Table Tennis",
          duration: "Nov 2020 - Mar 2024",
          description:
            " Winner in Table Tennis competitions, demonstrating exceptional sportsmanship and competitive spirit.",
        },
      ],
    };
  },
  computed: {
    firstColumnSkills() {
      return this.skills.slice(0, Math.ceil(this.skills.length / 2));
    },
    secondColumnSkills() {
      return this.skills.slice(Math.ceil(this.skills.length / 2));
    },
  },
};
</script>
  
  <style scoped>
.headline {
  font-size: 32px;
  font-weight: bold;
  margin-bottom: 25px;
  text-align: center;
}

.subheadline {
  font-size: 24px;
  font-weight: bold;
  margin-top: 20px;
  margin-bottom: 15px;
}

.v-list-item-title {
  font-weight: bold;
}

.mt-2 {
  margin-top: 0.5rem;
}
</style>
  