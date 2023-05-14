<template>
  <div id="app">
    <Scoreboard
      :currentPlayer="currentPlayer"
      :currentRound="currentRound"
      :currentScore="currentScore"
    />
    <Scores />
  </div>
</template>

<script>
import Scoreboard from "./components/Scoreboard.vue";
import ScoreInput from "./components/ScoreInput.vue";
import Scores from './components/Scores.vue'

export default {
  name: "App",
  components: {
    Scoreboard,
    Scores
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
  background-color: #eeeeee;
  width: 100%;
  height: 100%;
  min-height: 100vh;
}

</style>


