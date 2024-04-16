<template>
  <div class="username-form">
    <label for="username" class="username-label">Nombre de usuario:</label>
    <input type="text" id="username" v-model="state.username" class="username-input">
    <p>Caracteres antes: {{ characterCount.before }}</p>
    <p>Caracteres después: {{ characterCount.after }}</p>
  </div>
</template>

<script setup>
import { reactive, watch } from 'vue';

const state = reactive({
  username: '',
});

const characterCount = reactive({
  before: 0,
  after: 0
});


watch(() => state.username, (newValue, oldValue) => {
  characterCount.before = oldValue.length;
  characterCount.after = newValue.length;
});
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
