<template>
    <div class="login-form">
      <img alt=" logo" src="./../assets/logo.png"> <br>
      <h2 style="color: #61227D;">Welcome Back</h2>
      <p>Enter your email address and password to access your account.</p>
      <form @submit.prevent="login">
        <label for="email">Email Address</label>
  
        <input type="email" id="email" placeholder="Enter your email" v-model="email" required />
  
        <label for="password">Password</label>
        <input type="password" id="password" placeholder="Enter your password" v-model="password" required />
  
        <div class="remember-me">
          <input type="checkbox" id="remember" />
          <label for="remember">Remember me</label>
        </div>
  
        <button type="submit">Sign In</button>
      </form>
      <p>Don't have an Account? <router-link style="color: #61227D;" to="/signup">Sign Up</router-link></p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        email: '',
        password: '',
      };
    },
    methods: {
      login() {
       
      },
    },
  };
  </script>
  
  <style scoped>
  
  /* Mobile view (default) */
  .login-form {
    max-width: 400px;
    margin: 0 auto;
    padding: 20px;
    background-color: #ffffff;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  
  .login-form h2 {
    font-size: 24px;
    margin-bottom: 20px;
    color: #333;
  }
  
  .login-form form {
    display: flex;
    flex-direction: column;
  }
  
  .login-form label {
    font-size: 14px;
    margin-bottom: 8px;
    color: #555;
  }
  
  .login-form input[type="email"],
  .login-form input[type="password"] {
    padding: 10px;
    margin-bottom: 16px;
    border: 1px solid #ddd;
    border-radius: 4px;
    font-size: 14px;
  }
  
  .login-form button {
    background-color: #61227D;
    color: #fff;
    border: none;
    border-radius: 4px;
    padding: 12px;
    font-size: 14px;
    cursor: pointer;
  }
  
  .login-form button:hover {
    background-color: #61227D;
  }
  
  .login-form a {
    font-size: 12px;
    color: #888;
    text-decoration: none;
  }
  
  .login-form a:hover {
    text-decoration: underline;
  }
  </style>
  
  