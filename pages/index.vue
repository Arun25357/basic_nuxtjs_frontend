<template>
    <div class="home">
      <div class="content">
        <h1>Hello Welcome</h1>
        <div class="buttons">
          <NuxtLink to="/login" class="login-button">LOGIN</NuxtLink><br>
          <NuxtLink to="/register" class="register-button">REGISTER</NuxtLink>
        </div>
      </div>
    </div>
  </template>
  
  <style scoped>
  .home {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #094722;
    padding: 20px;
  }
  
  .content{
    text-align: center;
    max-width: 300px; /* Reduced maximum width */
    margin-top: 20px;
    width: 100%; /* Ensure full width within container */
    padding: 10px; /* Reduced padding */
    border: 1px solid #ccc;
    border-radius: 5px;
    background-color: #D3D3D3;
  }
  .buttons{

  }
  
  </style>
  