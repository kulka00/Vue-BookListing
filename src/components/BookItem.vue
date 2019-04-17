<template>
    <li>{{book.title}}:{{book.author}}</li>
</template>

<script>
export default {
name:BookItem,
props:['books']
}
</script>

<style>
li{
    display:block;
    margin: 0 10px;
}

</style>

