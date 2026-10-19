
<script setup>
import { ref, reactive } from 'vue';

const clicks = ref(0);

const person = reactive({
  naam: '',
  country: ''
});

function increment() {
  clicks.value++;
}

function changeCountry(country) {
  person.country = country;
}
</script>

<template>
  <div>
    <button @click="increment"> Klik mij </button>

    <button @click="changeCountry('Nederland')"> Nederland </button>

    <button @click="changeCountry('België')"> België </button>

    <input v-model="person.naam" placeholder="naam" />

    <p>De huidige waarde van de teller is: {{ clicks }}</p>
    <p>Het geselecteerde land is: {{ person.country }}</p>
    <p>Mijn naam is: {{ person.naam }}</p>
  </div>
</template>
