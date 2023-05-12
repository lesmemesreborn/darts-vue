<template>
  <div id="app">
    <Scoreboard
      :currentPlayer="currentPlayer"
      :currentRound="currentRound"
      :currentScore="currentScore"
    />
    <ScoreInput />
  </div>
</template>

<script>
import Scoreboard from "./components/Scoreboard.vue";
import ScoreInput from "./components/ScoreInput.vue";

export default {
  name: "App",
  components: {
    Scoreboard,
  },
  data() {
    return {
      currentPlayer: "Name",
      currentRound: 1,
      currentScore: 501,
    };
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
