<template>
    <div class="login-container">
      <div class="login-form">
        <h1>Login</h1>
        <NuxtLink to="/">HOME</NuxtLink><br>
        <label for="username">Username  :</label>
        <input type="text" name="username" v-model="login.username"><br>
        <label for="password">Password  :</label>
        <input type="password" name="password" v-model="login.password"><br>
  
        {{ login.username }} <br>
        {{ login.password }} <br>
  
        <button @click="submitLogin">Login</button> <br>
        <NuxtLink to="/register">Register</NuxtLink>
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  import { ref } from 'vue';
  import { useRouter } from 'vue-router';
  
  interface Login {
      username: string;
      password: string;
  }
  
  const login = ref<Login>({
      username: '',
      password: ''
  });
  
  const router = useRouter();
  
  const submitLogin = () => {

      if (login.value.username === 'arun' && login.value.password === '54321') {
          alert('Login successful!');
          router.push('/dashboard');
      } else {
          alert('Invalid username or password');
      }
  };
  </script>
  
  <style scoped>
  .login-container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #094722;
  }
  
  .login-form {
    width: 300px; /* Adjust width as needed */
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
    background-color: #D3D3D3;
  }
  
  </style>
  