<template>
    <div class="scores">
      <label for="score-input">Введите счет:</label>
      <div class="input-container">
        <input type="number" id="score-input" v-model.number="score" min="0" max="180" />
        <div class="keypad-container">
          <button v-for="num in numbers" :key="num" @click="addNumber(num)">{{ num }}</button>
          <button @click="addNumber(0)">0</button>
        </div>
      </div>
      <button @click="submitScore">Submit</button>
    </div>
  </template>
  
  <script>
  export default {
    name: "Scores",
    data() {
      return {
        score: 0,
        numbers: [1, 2, 3, 4, 5, 6, 7, 8, 9]
      };
    },
    methods: {
      addNumber(num) {
        this.score = Math.min(this.score * 10 + num, 180);
      },
      submitScore() {
        console.log("Submitted score:", this.score);
        this.score = 0;
      }
    }
  };
  </script>
  
  <style scoped>
  .scores {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 20px;
  }
  
  label {
    font-size: 24px;
    font-weight: bold;
    margin-bottom: 10px;
  }
  
  .input-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 10px;
  }
  
  input {
    font-size: 36px;
    width: 150px;
    text-align: center;
    padding: 10px;
    border: 2px solid #ccc;
    border-radius: 10px;
    outline: none;
    margin-right: 10px;
    margin-bottom: 15px;
  }
  
  .keypad-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(4, 1fr);
    grid-gap: 10px;
  }
  
  button {
    font-size: 28px;
    padding: 10px 15px;
    border: none;
    border-radius: 10px;
    background-color: #ccc;
    color: #fff;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #aaa;
  }
  
  button:nth-child(10) {
    grid-row: 4 / 5;
    grid-column: 2 / 3;
  }
  
  button:active {
    background-color: #999;
  }
  </style>