<template>
  <div id="app">
    <MainPage />
  </div>
</template>

<script>
import MainPage from "./components/MainPage.vue";

export default {
  name: "App",
  components: {
    MainPage
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Nunito:700,800|Poppins:500,700&display=swap");

:root {
  --var-dark-color: #383838;
  --var-light-color: #fff9f9;
  font-size: 60.5%;
}

html {
  height: 100vh;
}

body {
  margin: 0;
}

@media (max-width: 480px) {
  html,
  body {
    height: calc(100vh - 56px);
  }
}

@media only screen and (max-width: 1300px) {
  :root {
    font-size: 60%;
  }
}

@media only screen and (max-width: 425px) {
  :root {
    font-size: 50%;
  }
}
</style>
