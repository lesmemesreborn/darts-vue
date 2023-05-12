<template>
  <div class="scoreboard">
    <h2>Current Score:</h2>
    <div class="player">
      <h3>Player: {{ currentPlayer }}</h3>
    </div>
    <div class="round">
      <h3>Round: {{ currentRound }}</h3>
    </div>
    <div class="score">
      <h3>Score: {{ currentScore }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: "Scoreboard",
  props: {
    currentPlayer: {
      type: String,
      required: true,
    },
    currentRound: {
      type: Number,
      required: true,
    },
    currentScore: {
      type: Number,
      required: true,
    },
  },
};
</script>

<style scoped>
.scoreboard {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: 50px;
}

.player,
.round,
.score {
  margin: 10px;
}
</style>
