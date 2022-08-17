<template>
    <div class="card">
        <h3>Voiture</h3>
        <ul>
            <li>Prix : 15 000</li>
        </ul>
        <button class="btn" @click="count++">Ajouter au panier</button>
        <p>Vous avez ajouté {{ count }} voitures</p>
    </div>
</template>

<script setup lang="ts">
    import { ref } from 'vue';

    const count = ref(0);
</script>

<style scoped lang="scss">
.card {
    margin: 1rem;
    padding: 1.5rem;
    border-radius: 1rem;
    box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
    transition: .4s;
    &:hover {
        transform: scale(1.02) translateY(-.2rem);
    }
}
.btn {
    background-color: royalblue;
    color: white;
    padding: .5rem 1.5rem;

    border-radius: .5rem;
    border: 0;
    margin: .5rem .5rem .5rem 0;
    cursor: pointer;
    transition: .4s;

    &:hover {
        background-color:cornflowerblue;
    }
}
</style>