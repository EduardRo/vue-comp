
<template>
  <h3> Age {{ age }}</h3>
  <Greeting :age="age"></Greeting>
  <User v-bind:age="age" :name="name" @age-change="plusAg()"></User>
  <User v-bind:age="age" @age-change="age++"></User>
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
    },
    methods:{
      plusAg(){
        this.age=this.age+5;
        return age
      }
    }
   
};
</script>

