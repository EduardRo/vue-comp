<template>
    <div>
        <p>The user is {{ age }} years old and his name is {{ name }}</p>
        <button type="button" @click="onClickAge">Age User component</button>

    </div>
</template>

<script>
export default{
    name:'User',
    props:["age","name"],
    methods:{
        onClickAge(){
            this.$emit('age-change', 3)
        }
    }
}

</script>
