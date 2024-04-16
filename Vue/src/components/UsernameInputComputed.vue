<template>
    <div class="username-form">
      <label for="username" class="username-label">Nombre de usuario:</label>
      <input type="text" id="username" v-model="state.username" @input="validateUsername" class="username-input">
      <p :class="{ 'incorrect-username': !isUsernameValid, 'correct-name': isUsernameValid }">
        {{ usernameValidationMessage }}
      </p>
    </div>
</template>
  
<script setup>
  import { reactive, computed } from 'vue';
  
  const state = reactive({
    username: '',
  });
  
  const isUsernameValid = computed(() => {
    return state.username.length >= 5;
  });

  const usernameValidationMessage = computed(() => {
    return isUsernameValid.value ? '✅ - Nombre de usuario válido.' : '❌ - El nombre de usuario debe tener al menos 5 caracteres.';
  });

  function validateUsername() {
    // No es necesario modificar isUsernameValid directamente aquí, ya que está calculado dinámicamente por el computed.
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
