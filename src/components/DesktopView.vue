<template>
  <div class="login-container">
    <!-- Left Section -->
    <div class="left-section">
      <img alt=" logo" src="./../assets/logo.png">
      <img src="./../assets/header-image.png" alt="Team Achieve Logo" />
      <p>Your perfect solution for funding your desires</p>
    </div>

    <!-- Right Section -->
    <div class="right-section">
      <div class="login-card">
        <h2 style="color: #61227D;">Welcome Back</h2>
        <form @submit.prevent="login">
          <label for="email">Email Address</label>
          <input type="email" id="email" v-model="email" placeholder="Enter your email" required />
          <label for="password">Password</label>
          <input type="password" id="password" v-model="password" placeholder="Enter your password" required />
          <div class="remember-me">
            <input type="checkbox" id="remember" v-model="remember" />
            <label for="remember">Remember me</label>
          </div>
          <button type="submit">Sign In</button>
          <p class="forgot-password">
            <a href="#">Forgot Password?</a>
          </p>
        </form>
        <p class="signup-link">
          Don't have an account? <a href="#">Sign Up</a>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: "",
      password: "",
      remember: false,
    };
  },
  methods: {
    login() {
      // Implement your login logic here
      console.log("Logging in...");
    },
  },
};
</script>

<style scoped>

/* left section */
.left-section {

  background-color: #F8EAFF;
  color: #ffffff;
  padding: 50px;
  max-width: 50vmax;
  text-align: center;
}

.left-section h1 {
  font-size: 1.5rem;
}

.left-section img {
  max-width: 100%;
  margin-top: 20px;
}

/*right section */
.right-section {
  background-color: #FCFCFC;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
}

.login-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.login-card {
  background-color: #ffffff;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  width: 300px;
}

h2 {
  font-size: 1.5rem;
  margin-bottom: 20px;
}

label {
  font-weight: bold;
}

input {
  width: 100%;
  padding: 10px;
  margin-bottom: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

button {
  background-color: #61227D;
  color: #ffffff;
  border: none;
  border-radius: 4px;
  padding: 10px 20px;
  cursor: pointer;
}

.remember-me {
  display: flex;
  align-items: center;
  margin-bottom: 10px;
}

.forgot-password {
  text-align: center;
  margin-top: 10px;
}

.signup-link {
  text-align: center;
  margin-top: 20px;
}
</style>
