<template>
  <div class="login-form">
    <h2>Welcome Back</h2>
    <form @submit.prevent="login">
      <label for="email">Email Address</label>
      <input type="email" id="email" v-model="email" required />

      <label for="password">Password</label>
      <input type="password" id="password" v-model="password" required />

      <div class="remember-me">
        <input type="checkbox" id="remember" />
        <label for="remember">Remember me</label>
      </div>

      <button type="submit">Sign In</button>
    </form>
    <p>Don't have an Account? <router-link to="/signup">Sign Up</router-link></p>
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
  background-color: #6a63ff;
  color: #fff;
  border: none;
  border-radius: 4px;
  padding: 12px;
  font-size: 14px;
  cursor: pointer;
}

.login-form button:hover {
  background-color: #524de7;
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

