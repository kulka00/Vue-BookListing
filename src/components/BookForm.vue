<template>
<form v-on:submit.prevent="bookSubmit(bookTitle,bookAuther)"" class=""action="#" method="POST" >
    <input type="text" name="title"  value="" placeholder="Book Title">
    <input type="text" name="Author"  value="" placeholder="Book Author">
    <button type="submit" name="button"> Add book</button>
</form></template>

<script>
export default {
  name: "BookForm",
  props: ["books"],
  data() {
    return {
      bookTitle:'',
      bookAuther:''
    };
  },
  methods: {
      bookSubmit(bookTitle,bookAuther){
          this.$emit('addbook',bookTitle,bookAuther)
      }
  }
};
</script>

<style>
</style>
