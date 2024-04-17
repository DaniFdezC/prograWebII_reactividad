<script>
    import { writable } from 'svelte/store';
  
    const username = writable('');
    const isUsernameValid = writable(false);
  
    function validateUsername(event) {
      const inputUsername = event.target.value;
      isUsernameValid.set(inputUsername.length >= 5);
      username.set(inputUsername);
    }
  </script>
  
  <div class="username-form">
    <label for="username" class="username-label">Nombre de usuario:</label>
    <input type="text" id="username" bind:value={$username} on:input={validateUsername} class="username-input">
    {#if $isUsernameValid}
      <p class="correct-name">✅ - Nombre de usuario válido.</p>
    {:else}
      <p class="incorrect-username">❌ - El nombre de usuario debe tener al menos 5 caracteres.</p>
    {/if}
  </div>
  
  <style>
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
  