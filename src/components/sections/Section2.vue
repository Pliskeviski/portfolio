<template>
  <section class="section">
    <div class="text-content">
      <div class="section-info about-me">
        <div class="info-container">
          <h2 class="about-me-title">About me</h2>
          <div class="about-me-content">
            Jr. Software Engineer currently
            working at AutoTech where I mostly
            do front-end development.
            I’m also a full stack developer and
            a design enthusiast based on
            Curitiba, Brazil.
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
            <div class="familiar">
              But I'm also familiar with:
              <div class="familiar-tech">C++, ReactJS, VueJS, OpenGL, NodeJS, Ruby on Rails and many others!</div>
            </div>
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
          name: ".NET Framework/Core",
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
  height: 100%;
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
  margin-bottom: 35px;
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
