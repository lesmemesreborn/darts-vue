<template>
  <div class="scoreboard">
    <h2>Current Score:</h2>
    <div class="players"> 
      <div class="player player1">
        <h3>Player 1: {{ player1Score }}</h3>
      </div>
      <div class="player player2">
        <h3>Player 2: {{ player2Score }}</h3>
      </div>
    </div>
    <div class="round">
      <h3>Round: {{ currentRound }}</h3>
    </div>
  </div>
</template>
<script>
export default {
  name: "Scoreboard",
  props: {
    player1Score: {
      type: Number,
      required: true,
      default: 501,
    },
    player2Score: {
      type: Number,
      required: true,
      default: 501,
    },
    currentRound: {
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
  background-color: #f7f7f7;
  padding: 20px;
  box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.2);
}

.players {
  display: flex;
  flex-direction: row;
  justify-content: center;
  margin-top: 20px;
}

.player {
  display: flex;
  flex: 1;
  margin: 10px;
  justify-content: center;
  align-items: center;
  text-align: center;
  background-color: #fff;
  padding: 20px;
  box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.2);
}

.player:hover {
  transform: scale(1.05);
}

.player1 {
  border: 3px solid #bdc3c7;
}

.player2 {
  border: 3px solid #bdc3c7;
}
</style>