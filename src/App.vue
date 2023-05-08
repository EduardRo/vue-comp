
<template>
  <h3> from zeroo</h3>
  <Greeting :age="age"></Greeting>
  <User v-bind:age="age" :name="name"></User>
  
  <input type="number" v-model.number="age"/>
  <input type="text" v-model.lazy="name" />
  <card></card>
  <button type="button" v-on:click="age++">Add age</button>
  </template>


<script>
import Greeting from './components/Greeting.vue';
import Card from './components/Card.vue';
import User from './components/User.vue';


export default {
    name: "App",
    components:{
      Greeting:Greeting,
      Card:Card,
      User:User 

    },
    data(){
      return{
        age:20,
        name:''
      }
    }
   
};
</script>

