<script setup>
//import HelloWorld from './components/HelloWorld.vue'
//import TheWelcome from './components/TheWelcome.vue'
//import Button from './components/MyComponents/Button.vue'
//import Dialog from './components/MyComponents/Dialog.vue'
//import Footer from './components/MyComponents/Footer.vue'
import Header from './components/icons/MyComponents/Header.vue'
import Images from './components/icons/MyComponents/Images.vue'
import Calculator from './components/icons/MyComponents/Calculator.vue'
import Einkaufsliste from './components/icons/MyComponents/Einkaufsliste.vue'
import Bild from './components/icons/MyComponents/Bild.vue'

import { ref, computed } from 'vue';
const vorName = ref('')
const nachName = ref('')
const geburtsDatum = ref('')
const gender = ref('')
const name = computed(() => logPerson())

function logPerson() {
  return ('Vorname: ' + vorName.value + ', Nachname: ' + nachName.value + ' , Geburtsdatum: ' + geburtsDatum.value + ' , Geschlecht ist:  ' + gender.value)
};

//const einkaufsListe =ref([])


</script>


<template>
      <div id="cell1">
        <div>
          <div>
            <div id="logo">
              <Images />
            </div>
            <br>
            <div id="header">
              <Header />
            </div>
            <br>
            <div>
              <h2><strong> Dein Name lautet: </strong></h2> {{ name }}
            </div>
            <br>
            <div>
              <form>
                <input type="text" name="vorName" placeholder="Vorname" v-model="vorName" required>
                <input type="text" name="nachName" placeholder="Nachname" v-model="nachName" required>
                <input type="number" name="geburtsDatum" placeholder="Geburtsdatum" v-model="geburtsDatum" required>

                <select v-model="gender" required>
                  <option value="">Bitte wählen</option>
                  <option value="Male">Männlich</option>
                  <option value="Female">Weiblich</option>
                  <option value="Divers">Divers</option>
                </select>
              </form>
            </div>
            <br>
            <div>
              <button type="submit">Submit</button>
            </div>
            <br>
            <div>
              <Calculator />
            </div>
            <br>
            <div>
              <Einkaufsliste />
            </div>
          </div>
        </div>


      </div>
      <div id="cell2">
        <Bild />
      </div>
</template>

<style scoped>
header {
  line-height: 1.5;
  text-align: center;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}

#cell2{
  position: relative;
  display:flex;
  align-items: center;
  justify-content:center;
}

</style>
