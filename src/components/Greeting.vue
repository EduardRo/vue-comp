<template>
    <p v-if="(age>25)"> Greeting for this age mtf {{ age }}</p>
    <p v-else>You must be 25 years olders to view this message</p>
</template>

<script>
export default {
    name:'Greetings',
    data() {
        return {
            msg:"Greetngs to"
        }
    },
    props:["age"]
}

</script>
<style scoped lang="scss">
p:hover {
    color:darken(rgb(255, 0, 0),16%);
}
</style>
