<template>
  <div id="app">
    <enemy-fleets></enemy-fleets>
    <panel></panel>
    <my-fleets></my-fleets>
  </div>
</template>

<script>
import enemyFleets from "./components/enemyFleets.vue";
import panel from "./components/panel.vue";
import myFleets from "./components/myFleets.vue";

export default {
  name: "App",
  components: {
    enemyFleets,
    panel,
    myFleets,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  list-style: none;
}

html,
body {
  height: 100%;
  background-color: #fff;
}

body {
  width: 100%;
  position: relative;
  background-image: url("./assets/backgroun1.png");
  background-size: cover;
  background-position: 50% 50%;
}

#app {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  width: 1000px;
  height: 400px;
  display: flex;
}
</style>
