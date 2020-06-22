<template>
  <section class="section">
    <div class="text-content">
      <div class="section-info experience">
        <div class="info-container">
          <h2 class="experience-title">Experiences</h2>
          <div class="experience-content">
            <div v-for="item in experiences" :key="item.companyName" class="timeline-item">
              <h1>
                {{ item.companyName }}
                <br />
                {{ item.startEndDate }}
              </h1>
              <p>{{ item.description }}</p>
            </div>
          </div>
        </div>
      </div>
      <div class="section-info projects">
        <div class="info-container">
          <h2 class="projects-title">Projects</h2>
          <div class="projects-content">
            <div class="check-github">
              <p>Check out my GitHub profile:</p>
              <a href="https://github.com/Pliskeviski" target="_blank">
                <div class="github-image"></div>
              </a>
              <div class="github-name">Pliskeviski</div>
              <div class="email">
                Reach out to me:
                <br /><a href="mailto:gustavopliskeviski@gmail.com">gustavopliskeviski@gmail.com</a>
              </div>
            </div>
            <div class="find-me-on">
              Find me on:
              <div class="social">
                <a href="https://www.linkedin.com/in/pliskeviski/" target="_blank">
                  <i class="fa fa-linkedin-square fa-3x"></i>
                </a>
                <a href="https://github.com/Pliskeviski" target="_blank">
                  <i class="fab fa-github fa-4x"></i>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Section3",
  data() {
    return {
      experiences: [
        {
          companyName: "Sisteplan Softwares.",
          startEndDate: "Oct. 2018 - Oct. 2019.",
          description:
            "Had the opportunity to work as a full stack developer using .NET Framework and Angular 6. Mainly working on government projects."
        },
        {
          companyName: "AutoTech.",
          startEndDate: "Oct. 2019 - Apr. 2020",
          description:
            "Working mainly as a front-end developer using Angular 8, AngularJS, .NET and ASP.NET MVC. Most projects were focused on auctions."
        },
        {
          companyName: "Manipulaê.",
          startEndDate: "Apr. 2020 - Present.",
          description:
            "Working remotely as a full-stack developer using ReactJS, React Native and .NET Core. Working on a SaaS project focused on pharmacies."
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

.experience {
  background: var(--var-dark-color);
  font-family: "Nunito", sans-serif;
}

.projects {
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
  font-size: 48px;
  font-family: "Poppins", sans-serif;
  margin: 0;
  margin-bottom: 35px;
}

.experience-title {
  color: var(--var-light-color);
}

.experience-content {
  color: var(--var-light-color);
  font-weight: normal;
}

.projects-title {
  text-align: center;
}

.timeline-item {
  padding: 0.8em 3em 2em 2em;
  position: relative;
  color: rgba(black, 0.7);
  border-left: 2px solid var(--var-light-color);
  font-family: "Poppins", sans-serif;
  font-weight: 800;
}

.timeline-item h1 {
  margin-top: 0;
  font-size: 2rem;
}

.timeline-item p {
  font-size: 1.1rem;
  font-family: "Nunito", sans-serif;
}

.timeline-item::before {
  position: absolute;
  left: 2em;
  font-weight: bold;
  top: 1em;
  display: block;
  font-family: "Poppins", sans-serif;
  font-weight: 800;
  font-size: 0.785rem;
}

.timeline-item::after {
  width: 10px;
  height: 10px;
  display: block;
  top: 1em;
  position: absolute;
  left: -7px;
  border-radius: 10px;
  content: "";
  border: 2px solid var(--var-light-color);
  background: white;
}

.timeline-item:last-child {
  border-image: linear-gradient(
      to bottom,
      var(--var-light-color) 60%,
      rgba(var(--var-light-color), 0)
    )
    1 100%;
}

.projects-content {
  flex: auto;
  display: flex;
  flex-direction: column;
}

.check-github {
  flex: 1;
  align-self: center;
  text-align: center;
}

.check-github p {
  font-weight: 800;
  font-size: 1.1rem;
  padding-bottom: 10px;
}

.check-github i {
  color: var(--var-dark-color);
  padding: 10px;
}

.github-image {
  height: 180px;
  width: 180px;
  border-radius: 100px;
  background: url("https://github.com/Pliskeviski.png?size=180");
}

.github-name {
  font-size: 2.6rem;
  padding-top: 20px;
  font-weight: 500;
}

.find-me-on {
  font-weight: 800;
  text-align: center;
  flex: 0.4;
  display: flex;
  flex-direction: column;
  font-size: 1.4rem;
}

.find-me-on i {
  color: var(--var-dark-color);
  font-size: 3em;
  padding: 10px;
}

.email {
  padding-top: 15px;
}

.email a {
  color: var(--var-dark-color);
  text-decoration: none;
}

@media only screen and (max-width: 1024px) {
  .text-content {
    flex-direction: column;
  }
}

@media only screen and (max-width: 425px) {
  h2 {
    font-size: 41px;
  }
}
</style>
