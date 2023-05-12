<template>
  <div class="score-input">
    <h2>Enter Score:</h2>

    <div class="score-form">
      <form @submit.prevent="onSubmit">
        <label for="score">Score:</label>
        <input type="number" id="score" v-model="score" required />
        <button type="submit">Submit</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "ScoreInput",
  components: {},
  data() {
    return {
      score: null,
    };
  },
  methods: {
    onSectorSelected(sector) {
      // Обработка выбранного сектора на дартс-доске
    },
    onSubmit() {
      // Обработка введенного количества очков
      this.score = null;
    },
  },
};
</script>

<style scoped>
.score-input {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: 50px;
}

.dartboard {
  margin: 10px;
}

.score-form {
  margin: 10px;
}

form {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}

label {
  margin-right: 10px;
}
</style>
