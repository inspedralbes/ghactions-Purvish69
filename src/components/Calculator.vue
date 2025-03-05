<template>
    <div class="calculator-container">
      <h1>Purvish</h1>
      <h2>Mi Calculadora</h2>
      <div class="keyboard">
        <button v-for="number in numbers" :key="number" @click="handleClick(number)">
          {{ number }}
        </button>
      </div>
      <p>Has clicat el número: {{ clickedNumber }}</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        numbers: [1, 2, 3, 4, 5, 6, 7, 8, 9],
        clickedNumber: null,
      };
    },
    methods: {
      handleClick(number) {
        this.clickedNumber = number;
      },
    },
  };
  </script>
  
  <style>

  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    
  }

  body {
    font-family: Arial, sans-serif;
    background: linear-gradient(135deg, #71b7e6, #9b59b6);
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
    margin-left: 700px;
  }
  

  .calculator-container {
    background: #552e2e;
    border-radius: 10px;
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
    padding: 20px;
    width: 300px;
    text-align: center;
  }
  
 
  h1 {
    color: #ffffff;
    margin-bottom: 10px;
  }
  
  h2 {
    color: #ffffff;
    margin-bottom: 20px;
  }
  

  .keyboard {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
    margin-bottom: 20px;
  }

  button {
    background: #4caf50;
    color: #fff;
    border: none;
    border-radius: 5px;
    padding: 15px;
    font-size: 18px;
    cursor: pointer;
    transition: background 0.3s ease, transform 0.2s ease;
  }
  
  button:hover {
    background: #45a049;
    transform: scale(1.05);
  }
  
  /* Texto de resultado */
  p {
    font-size: 16px;
    color: #ffffff;
  }
  </style>
  