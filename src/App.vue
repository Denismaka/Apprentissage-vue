<!-- ################# -->
<!-- La syntaxe Vue Js -->
<!-- ################# -->
/* Voici un exemple de compteur simple en Vue.js. Le compteur commence à 0 et
s'incrémente de 1 toutes les secondes grâce à la fonction setInterval. Vous
pouvez également ajouter des boutons pour incrémenter ou décrémenter
manuellement le compteur. */
<template>
    <p>compteur : {{ count }}</p>
    <div v-show="count >= 5">Bravo vous avez cliqué plus de 5 fois !</div>
    <button @click="increment">Incrémenter</button>
    <button @click="decrement">Decrémenter</button>
</template>

<script setup>
import { ref } from "vue";

const count = ref(0);

const increment = (event) => {
    console.log(event);
    count.value++;
};
const decrement = () => {
    count.value--;
};
</script>

<style>
button {
    padding: 10px;
    background-color: #3498db;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-family: Roboto, sans-serif;
}
button:last-child {
    margin-left: 10px;
}
button:hover {
    background-color: #2980b9;
}
p {
    font-size: 24px;
    font-weight: bold;
    font-family: Roboto, sans-serif;
}
div[v-show] {
    margin-top: 10px;
    font-size: 18px;
    color: #2ecc71;
    font-family: Roboto, sans-serif;
}
</style>

<!-- ########################### -->
<!-- TP  Todolist avec Vue js    -->
<!-- ########################### -->
