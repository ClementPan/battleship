<template>
  <div class="panel">
    <div class="instruction">
      <h2>Welcome on board, sir!</h2>
    </div>
    <button v-if="!gameOn" class="controlBtn" @click="createNewGame">
      New Battle!
    </button>
    <button v-else class="controlBtn">
      {{ hitNumbers }} : {{ firedNumbers }}
    </button>
    <div class="record">
      <ul class="record-list">
        <li class="record-item" v-for="item in battleRecord" :key="item">
          <p>{{ item }}</p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.panel {
  width: 180px;
  margin: 0 10px;
  display: flex;
  flex-direction: column;
  text-align: center;
  background-color: #fff;
  opacity: 0.8;
}
.instruction {
  height: 80px;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #aaa;
  color: #111;
}
h2 {
  color: #333;
  font-size: 24px;
}

.controlBtn {
  height: 40px;
  width: 100%;
  font-size: 28px;
  color: #ddd;
  background-color: #800888;
}
.controlBtn:hover {
  cursor: pointer;
}
.record {
  background-color: #eee;
  height: calc(400px - 120px);
  overflow-y: hidden;
}
.record-list {
  padding: 4px;
}
.record-item:first-child {
  background-color: red;
  height: 40px;
  font-size: 16px;
  color: #fff;
  line-height: 40px;
}
</style>