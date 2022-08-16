<template>
  <div class="card" @click="userClick('card')">
    <h1>Ma Card</h1>
    <button class="button" @click.stop="userClick('btn')">Mon bouton</button>
  </div>
</template>

<script setup lang="ts">

  function userClick(from: string) {
    console.log('click from', from);
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
