<template>
    <div class="username-form">
      <label for="username" class="username-label">Nombre de usuario:</label>
      <input type="text" id="username" v-model="state.username" @input="validateUsername" class="username-input">
      <p :class="{ 'incorrect-username': !state.isUsernameValid, 'correct-name': state.isUsernameValid }">
        {{ state.isUsernameValid ? '✅ - Nombre de usuario válido.' : '❌ - El nombre de usuario debe tener al menos 5 caracteres.' }}
      </p>
    </div>
</template>
  
<script setup>
  import { reactive } from 'vue';
  
  const state = reactive({
    username: '',
    isUsernameValid: false
  });
  
  function validateUsername() {
    state.isUsernameValid = state.username.length >= 5;
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
