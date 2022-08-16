<template>
  <div class="card">
    <h1>Bonjour {{ state.user.name }}</h1>
    <p>Count : {{ state.count }}</p>
    <button class="button" @click="userClick()">Incrémenter</button>
  </div>
</template>

<script setup lang="ts">
  import { reactive } from 'vue';

  const state = reactive({
    user: {
      name: 'Nicolas',
      age:35
    },
    count: 0
  })

  setTimeout(()=> {
    state.user.name = "Pauline";
  }, 2000)


  function userClick() {
    state.count++;
  }

</script>

<style>
.card {
  background-color:azure;
  border-radius: 1rem;
  padding: 1rem;
  cursor: pointer;
}
.button {
  border-radius: .5rem;
  padding: .5rem 1rem;
  border: 0;
  cursor: pointer;
}
</style>
