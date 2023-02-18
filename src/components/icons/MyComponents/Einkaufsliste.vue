<template>
    <h2>Meine EinkaufsListe</h2>
    <img src="https://lerneprogrammieren.de/wordpress/wp-content/uploads/einkaufswagen.png" height="35px"/>
    <div>
        <input id="benutzerInput" type="text" placeholder="Neues Item" v-model="newItem">
        <input id="benutzerInput" type="number" placeholder="Preis in Euro" v-model="newPrice">
        <button id="enter" type = "button" @click="hinzufügen">Hinzufügen</button>
        <ul>
            <li v-for="(item, preis) in allItems">{{ item, preis }}</li>
        </ul>
    </div>
</template>

<script setup>
import { ref } from 'vue';

//import {ref} from 'vue'
const newItem = ref('')
const newPrice=ref('')
const allItems=ref([])
const allPrices=ref([])

function hinzufügen(){
    console.log(newItem.value, newPrice.value);
    allItems.value.push(newItem.value + ' ' + newPrice.value + ' Euro');
    newItem.value="";
    newPrice.value="";
}

</script>
<style></style>