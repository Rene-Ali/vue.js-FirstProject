<template>
    <h2>Mein Cash-Flowrechner</h2>
    <form>
        <input type="number" placeholder="Mein Budget" v-model="budget">
        <button @click="budgetBerechnen()">Budget berechnen</button>
        <p>Du hast noch xyz Euro zur Verfügung.</p>
    </form>
</template>

<script>
import { ref } from 'vue';
/*import Einkaufsliste from './Einkaufsliste.vue';

const restBudget = ref('');

/*function budgetBerechnen(){
    restBudget = sum.value - budget.value;
    console.log(restBudget);
}*/


//function alarm(){
   // alert("You are broke")


/*methods:{
    if ()
}*/

</script>
<style>
p{
    text-align: left;
    padding-top: 10px;
    background-color: lightgrey;
    font-weight: 800;
}
</style>