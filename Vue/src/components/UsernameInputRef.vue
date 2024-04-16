<template>
    <div class="username-form">
      <label for="username" class="username-label">Nombre de usuario:</label>
      <input type="text" id="username" v-model="username" @input="validateUsername" class="username-input">
        <!--  
            Dependiendo de cuántos caracteres se hayan escrito, se le otorga una clase u otra
            lo comprobams llamando a la función validateUsername
        -->
      <p :class="{ 'incorrect-username': !isUsernameValid, 'correct-name': isUsernameValid }">
        {{ isUsernameValid ? '✅ - Nombre de usuario válido.' : '❌ - El nombre de usuario debe tener al menos 5 caracteres.' }}
      </p>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const username = ref('');
  const isUsernameValid = ref(false);
  
  function validateUsername() {
    isUsernameValid.value = username.value.length >= 5;
  }
  </script>
  
  <style scoped>
  .username-form {
    margin-bottom: 20px;
  }
  
  .username-label {
    margin-bottom: 8px;
    margin-right: 20px;
  }
  
  .username-input {
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
  .incorrect-username {
    color: red;
    font-size: 14px;
  }

  .correct-name {
    color: green;
  }
  </style>
  