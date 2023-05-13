
<template>
  <h3> Age {{ age }}</h3>
  <Greeting :age="age"></Greeting>
  <User v-bind:age="age" v-bind:name="name" @age-change="plusAg" />
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

