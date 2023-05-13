<template>
    <div>
        <p>The user is {{ age }} years old and his name is {{ createName }}</p>
        <button type="button" @click="onClickAge">Age User component</button>
        <h2>Age Doubled: {{ ageDoubled }}</h2>

    </div>
</template>

<script>
export default{
    name:'User',
    props:{
        age:{type:Number, required:false, validator(value){return value<130}},
        firstname:{type:String},
        lastname:{type:String},

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
