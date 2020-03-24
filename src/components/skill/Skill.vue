<template>
  <div class="item-skill">
    <div class="skill-title">{{name}}</div>
    <div class="skill-progress">
      <div class="progress-bar">
        <span class="inner-progress" v-bind:style="{ width: percentage + '%' }"></span>
      </div>
      <span class="skill-percentage">{{percentage}}%</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "Skill",
  props: {
    name: String,
    percentage: Number
  }
};
</script>

<style scoped>
.item-skill {
  margin-bottom: 20px;
  font-weight: 800;
}

.skill-title {
  font-size: 2.1rem;
  margin-bottom: 7px;
}

.skill-progress {
  display: flex;
  flex-direction: row;
}

.progress-bar {
  height: 25px;
  position: relative;
  background-color: var(--var-dark-color);
  -moz-border-radius: 25px;
  -webkit-border-radius: 25px;
  border-radius: 25px;
  padding: 2px;
  width: 85%;
}

.inner-progress {
  background: var(--var-light-color);
  display: block;
  height: 100%;
  -moz-border-radius: 25px;
  -webkit-border-radius: 25px;
  border-radius: 25px;
  position: relative;
  overflow: hidden;
}

.skill-percentage {
  align-self: center;
  font-size: 1.9rem;
  padding-left: 10px;
}

.skills-content {
  font-weight: 800;
}
</style>
