<template>
    <h2>Mein Cash-Flowrechner</h2>
    <form v-on:submit.prevent="add">
        <input type="number" placeholder="Mein Budget" v-model="num1">
        <input type="number" placeholder="Meine Ausgaben" v-model="num2">
        <button type="submit">
            Substract
        </button>
    </form>
    <p>Result: {{ sum }}</p>
</template>

<script>
import Einkaufsliste from './Einkaufsliste.vue';
import { ref } from 'vue';


export default {
    data() {
      return {
        num1: '',
        num2: '',
        sum: '',
      };
    },
    methods:{
        add:function() {this.sum = parseInt(this.num1, 10) - parseInt(this.num2, 10);
    }
}
};
</script>
<style></style>