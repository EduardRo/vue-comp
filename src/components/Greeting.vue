<template>
    <p>
{{ msg }}
    </p>
</template>

<script>
export default {
    name:'Greetings',
    data() {
        return {
            msg:"Greetngs to"
        }
    },
}

</script>
<style scoped lang="scss">
p:hover {
    color:darken(rgb(255, 0, 0),16%);
}
</style>
