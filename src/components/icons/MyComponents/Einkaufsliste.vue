<template>
    <h2>Meine EinkaufsListe</h2>
    <img src="https://lerneprogrammieren.de/wordpress/wp-content/uploads/einkaufswagen.png" height="35px"/>
    <div>
        <input id="benutzerInput" type="text" placeholder="Neues Item" v-model="newItem.name">
        <input id="benutzerInput" type="number" placeholder="Preis in Euro" v-model="newItem.price">
        <button id="enter" type = "button" @click="hinzufügen">Hinzufügen</button>
        <ul>
            <li v-for="item in allItems">{{ item.name }} kostet {{ item.price }} €</li>
        </ul>
    </div>
</template>

<script setup>
import { ref } from 'vue';


//import {ref} from 'vue'
//const newItem = ref('')
//const newPrice=ref('')
const newItem=ref({
    name: '',
    price: ''
});

const allItems=ref([]);
const sum=ref(0);

function hinzufügen(){
    //allItems.value.push(newItem.value + ' ' + newPrice.value + ' Euro');
    console.log(newItem.value);
    allItems.value.push({...newItem.value});
    sum.value += newItem.value.price;
    newItem.value.name='';
    newItem.value.price='';
    console.log(allItems.value);
    console.log(sum.value);
    
};

/*export default{
    name: 'Einkaufsliste',
    methods: {
        budgetBerechnen: 
    }
}*/


</script>
<style></style>