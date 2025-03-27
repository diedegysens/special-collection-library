<template>
    <div class="container">
      <div class="logo">
        <h1>sint<br />— lukas<br />bibliotheek</h1>
      </div>
      <div class="form-container">
        <form @submit.prevent="submitForm">
          <div class="input-group">
            <label for="firstName">first name:</label>
            <input id="firstName" type="text" v-model="firstName" disabled />
          </div>
  
          <div class="input-group">
            <label for="lastName">last name:</label>
            <input id="lastName" type="text" v-model="lastName" disabled />
          </div>
  
          <div class="input-group">
            <label for="password">password:</label>
            <input id="password" type="password" v-model="password" required />
          </div>
  
          <div class="input-group">
            <label for="confirmPassword">confirm password:</label>
            <input id="confirmPassword" type="password" v-model="confirmPassword" required />
          </div>
  
          <div class="checkbox-group">
            <input id="terms" type="checkbox" v-model="termsAccepted" />
            <label for="terms">accept terms of conditions</label>
          </div>
  
          <button type="submit" :disabled="!termsAccepted">sign in</button>
  
          <p>Already have an account? <a href="/login">Log in</a></p>
        </form>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        firstName: "Diede",
        lastName: "Gysens",
        password: "",
        confirmPassword: "",
        termsAccepted: false,
      };
    },
    methods: {
      submitForm() {
        if (this.password !== this.confirmPassword) {
          alert("Passwords do not match!");
          return;
        }
        alert("Registration successful!");
      },
    },
  };
  </script>
  
  <style scoped>
  .container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    font-family: serif;
  }
  
  .logo {
    text-align: center;
    font-size: 24px;
    font-weight: bold;
  }
  
  .form-container {
    background: #fff;
    padding: 20px;
    border-radius: 10px;
    width: 300px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  }
  
  .input-group {
    display: flex;
    flex-direction: column;
    margin-bottom: 15px;
  }
  
  .input-group label {
    font-size: 14px;
    color: #333;
  }
  
  .input-group input {
    padding: 10px;
    border: 1px solid #0505057a;
    border-radius: 5px;
    font-size: 16px;
  }
  
  .checkbox-group {
    display: flex;
    align-items: center;
    margin-bottom: 15px;
  }
  
  .checkbox-group input {
    margin-right: 5px;
  }
  
  button {
    background: black;
    color: white;
    padding: 10px;
    border: none;
    border-radius: 5px;
    width: 100%;
    cursor: pointer;
  }
  
  button:disabled {
    background: rgb(0, 0, 0);
    cursor: not-allowed;
  }
  
  p {
    text-align: center;
    margin-top: 10px;
  }
  
  p a {
    color: black;
    text-decoration: underline;
  }
  </style>
  