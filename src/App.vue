
<template>
  <p> from zeroo</p>
  <greeting></greeting>
  <h2>{{ msg }}</h2>
  <card></card>
  </template>


<script>
import Greeting from './components/Greeting.vue';
import Card from './components/Card.vue';


export default {
    name: "App",
    components:{
      Greeting:Greeting,
      Card:Card,

    }
   
};
</script>

