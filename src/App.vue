
<template>
  <h3> Age {{ age }}</h3>
  <Greeting :age="age"></Greeting>
  <User v-bind:age="age" v-bind:firstname="firstName" :lastname="lastName" @age-change="plusAg" />
  <User v-bind:age="age" @age-change="age++"></User>
  <input type="number" v-model.number="age"/>
  <label>First Name</label>
  <input type="text" v-model.lazy="firstName" />
  <label>Last Name</label>
  <input type="text" v-model.lazy="lastName" />
  <card></card>
  <button type="button" v-on:click="age++">Add age</button>
  </template>


<script>
import Greeting from './components/Greeting.vue';
import Card from './components/Card.vue';
import User from './components/User.vue';
import MyCard from './components/MyCard.vue';


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
        firstName:'Emil',
        lastName:'Buran',
        name:''
      }
    },
    methods:{
      plusAg(num){
        this.age=this.age+num;
        //return age
      }
    }
   
};
</script>

