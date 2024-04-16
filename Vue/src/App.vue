<script setup>
import UsernameInputRef from './components/UsernameInputRef.vue';
import UsernameInputReactive from './components/UsernameInputReactive.vue';
import UsernameInputWatch from './components/UsernameInputWatch.vue';
import UsernameInputComputed from './components/UsernameInputComputed.vue';

</script>

<template>
  <div id ="#app">
    <h1> Ejemplo ref </h1>
    <UsernameInputRef />
    <br><br><br><br><br><br>
    <h1> Ejemplo reactive </h1>
    <UsernameInputReactive />
    <br><br><br><br><br><br>
    <h1> Ejemplo computed </h1>
    <UsernameInputComputed />
    <br><br><br><br><br><br>
    <h1> Ejemplo watch </h1>
    <UsernameInputWatch />
  </div>
</template>