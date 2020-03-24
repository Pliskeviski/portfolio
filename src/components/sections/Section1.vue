<template>
  <section class="section">
    <div class="info-header">
      <h2 class="info-name">{{nameInfo}}</h2>
    </div>
    <div class="text-content">
      <h1 data-aos="fade" class="hello">HELLO</h1>
    </div>
    <div class="scroll-down" data-aos="zoom-in" data-aos-anchor=".hello">
      <p>Scroll</p>
      <i class="fas fa-arrow-down"></i>
    </div>
  </section>
</template>

<script>
export default {
  name: "Section1",
  data() {
    return {
      nameInfo: "Gustavo Pliskeviski. Curitiba/PR, Brazil."
    };
  }
};
</script>

<style scoped>
.section {
  width: 100%;
  height: 100%;
  display: flex;
  flex-flow: column;
  scroll-snap-align: start;
}

.info-header {
  min-height: 40px;
  display: flex;
  flex-flow: column;
  justify-content: center;
}

.info-name {
  font-family: "Nunito", sans-serif;
  font-weight: 800;
  font-size: 1.4rem;
  margin: 0;
}

.text-content {
  height: 100%;
  flex: auto;
  display: flex;
  background-color: var(--var-dark-color);
  align-items: center;
  justify-content: space-around;
}

.hello {
  text-align: center;
  font-family: "Poppins", sans-serif;
  font-weight: bold;
  font-size: 15vw;
  color: var(--var-dark-color);
  -webkit-text-stroke-width: 1px;
  -webkit-text-stroke-color: var(--var-light-color);
  cursor: default;
}

.scroll-down {
  position: absolute;
  font-family: "Poppins", sans-serif;
  font-weight: bold;
  bottom: 25px;
  color: var(--var-light-color);
  display: flex;
  align-items: center;
  height: 0;
}

.scroll-down p {
  margin: 0;
  transform: rotate(90deg);
}

@media only screen and (max-width: 798px) {
  .hello {
    font-size: 25vw;
  }
}
</style>
