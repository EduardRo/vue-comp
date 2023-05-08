<template>
    <div>
        <p>The user is {{ age }} years old and his name is {{ name }}</p>

    </div>
</template>

<script>
export default{
    name:'User',
    props:["age","name"]
}

</script>
