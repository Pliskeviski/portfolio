<template>
  <section class="section">
    <div class="text-content">
      <div class="section-info about-me">
        <div class="info-container">
          <h2 class="about-me-title">About me</h2>
          <div class="about-me-content">
            I’m Gustavo Pliskeviski,
            currently working as a
            full-stack developer at Manipulaê.
            I’ve been doing and studying software development
            for the past 7 years and learned a lot
            with different projects and clients.
            I’m also a design enthusiast living
            in Curitiba, Brazil.
          </div>
        </div>
      </div>
      <div class="section-info skills">
        <div class="info-container">
          <h2 class="skills-title">Technologies</h2>
          <div class="skills-content">
            <div class="confident-text">How confident I fell about:</div>
            <Skill
              v-for="item in skills"
              :key="item.name"
              :name="item.name"
              :percentage="item.percentage"
            ></Skill>
          </div>
          <div class="familiar">
            But I'm also familiar with:
            <div class="familiar-tech">C++, VueJS, OpenGL, NodeJS, Ruby on Rails and many others!</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Skill from "../skill/Skill.vue";

export default {
  name: "Section2",
  components: {
    Skill
  },
  data() {
    return {
      skills: [
        {
          name: ".NET Core",
          percentage: 88
        },
        {
          name: "Angular 2+",
          percentage: 90
        },
        {
          name: "HTML & CSS",
          percentage: 95
        },
        {
          name: "React Native",
          percentage: 75
        },
        {
          name: "ReactJS",
          percentage: 85
        }
      ]
    };
  }
};
</script>

<style scoped>
.section {
  width: 100%;
  display: flex;
  flex-flow: column;
}

.text-content {
  flex: auto;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-around;
}

.section-info {
  flex: 1;
  min-height: 100vh;
  width: 100%;
  display: flex;
  justify-content: space-around;
  scroll-snap-align: start;
}

.about-me {
  background: var(--var-dark-color);
  font-family: "Nunito", sans-serif;
}

.skills {
  background: var(--var-light-color);
  font-family: "Poppins", sans-serif;
  color: var(--var-dark-color);
}

.info-container {
  display: flex;
  flex-direction: column;
  width: 40%;
  min-width: 298px;
  padding-top: 5%;
}

h2 {
  font-weight: 800;
  font-size: 4.8rem;
  font-family: "Poppins", sans-serif;
  margin: 0;
  margin-bottom: 35px;
}

.about-me-title {
  color: var(--var-light-color);
}

.about-me-content {
  color: var(--var-light-color);
  font-weight: normal;
  font-size: 1.4rem;
}

.confident-text {
  font-weight: 800;
  font-size: 1.4rem;
  margin-bottom: 30px;
}

.familiar {
  font-weight: bold;
  font-size: 1.1rem;
}

.familiar-tech {
  font-weight: normal;
  font-size: 1rem;
}

@media only screen and (max-width: 1024px) {
  .text-content {
    flex-direction: column;
  }
}
</style>
