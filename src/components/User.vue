<template>
    <div>
        <p>The user is {{ age }} years old and his name is {{ createName }}</p>
        <button type="button" @click="onClickAge">Age User component</button>
        <h2>Age Doubled: {{ ageDoubled }}</h2>
        <button type="button" @click="ageChangeFn(ageChange)">Age User component using callback function</button>
        <div>
            <label>number to change the age from user component</label>
        <input type="number" v-model.lazy="ageChange">
        </div>
        
    </div>
</template>

<script>
export default{
    name:'User',
    data(){
        ageChange:{Number}
    },
    props:{
        age:{type:Number, required:false, validator(value){return value<130}},
        firstname:{type:String},
        lastname:{type:String},
        ageChangeFn:Function,

    },
    emits:['age-change'],
    computed:{
        createName(){
            return this.firstname+' '+this.lastname

        },
        ageDoubled(){
            return this.age*2
        }
    },
    methods:{
        onClickAge(){
            this.$emit('age-change', 3)
        }
    }
}

</script>
