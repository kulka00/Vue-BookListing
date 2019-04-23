<template>
<form v-on:submit.prevent="bookSubmit(bookTitle,bookAuther)" class=""action="#" method="post" >
    <input v-model="bookTitle" type="text" name="title"  value="" placeholder="Book Title">
    <input v-model="bookAuthor" type="text" name="Author"  value="" placeholder="Book Author">
    <button type="submit" name="button"> Add book</button>
</form></template>

<script>
export default {
  name: "BookForm",
  props: ["books"],
  data() {
    return {
      bookTitle:'',
      bookAuthor:''
    };
  },
  methods: {
      bookSubmit(bookTitle,bookAuther){
          this.$emit('addBook',bookTitle,bookAuther)
      }
  }
};
</script>

<style>
</style>
