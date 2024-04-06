<template>
  <div class="register-container">
    <div class="register-form">
      <h1>Register</h1>
      <NuxtLink to="/">HOME</NuxtLink><br>
      <label for="email">Email</label>
      <input type="text" name="email" v-model="register.email"><br>
      <label for="username">Username</label>
      <input type="text" name="username" v-model="register.username"><br>
      <label for="password">Password</label>
      <input type="password" name="password" v-model="register.password"><br>

      {{ register.email }} <br>
      {{ register.username }} <br>
      {{ register.password }} <br>

      <button @click="submitRegister">Register</button> <br>
      <NuxtLink to="/login">Login</NuxtLink>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import { useRouter } from 'vue-router';

interface Register {
  email: string;
  username: string;
  password: string;
}

const register = ref<Register>({
  email: '',
  username: '',
  password: ''
});

const router = useRouter();

const submitRegister = () => {
  // Simulate registration logic
  if (register.value.email === 'arun.@kkumail.com' && register.value.username === 'arun' && register.value.password === '12345') {
    alert('Registration successful!');
    router.push('/dashboard');
  } else {
    alert('Invalid email, username, or password');
  }
};
</script>

<style scoped>
.register-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #094722;
}

.register-form {
  width: 300px; /* Adjust width as needed */
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  background-color: #D3D3D3;
}
</style>
