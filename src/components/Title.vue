<template>
    <h1>{{ title }}</h1>
</template>

<script>
export default {
    props: {
        title : String,
    }
}
</script>

<style scoped>
h1{
    color : #42b983;
    text-align: center;
}
</style>
