<template>
  <div class="enemyFleets">
    <div class="screenLock" v-if="!gameOn"></div>
    <div id="field">
      <div
        class="spot"
        v-for="spot in field"
        @click="fire(spot)"
        :class="spot.stat"
        :key="spot.id"
      >
        <i class="fas fa-water" v-if="spot.stat === 'spared'"></i>
        <i class="fas fa-water" v-else-if="spot.stat === 'fired'"></i>
        <i class="fas fa-water" v-else-if="spot.stat === 'loaded'"></i>
        <i class="fas fa-fire-alt" v-else-if="spot.stat === 'hit'"></i>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.enemyFleets {
  width: 400px;
  height: 400px;
  position: relative;
}
.screenLock {
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: 999;
}

#field {
  display: flex;
  flex-flow: row wrap;
  border-radius: 10px;
  background-color: rgba(133, 135, 133, 0.3);
}
.spot {
  border-radius: 20px;
  width: 40px;
  height: 40px;
  background-color: grey;
  text-align: center;
  line-height: 50px;
  font-size: 18px;
  color: #fff;
  opacity: 0.8;
  display: flex;
  align-items: center;
  justify-content: center;
}
.spot:hover {
  background-color: #f60;
  cursor: pointer;
}
.spot .hit {
  background-color: red;
}
.spot .fired {
  background-color: blue;
}
</style>