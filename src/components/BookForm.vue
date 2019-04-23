<template>
<form v-on:submit.prevent="bookSubmit(bookTitle,bookAuthor)" class=""action="#" method="post" >
    <input v-model="bookData.bookTitle" type="text" name="title"  value="" placeholder="Book Title">
    <input v-model="bookData.bookAuthor" type="text" name="Author"  value="" placeholder="Book Author">
    <div>
        <input type="checkbox" v-model="bookData.finishedReading">
    </div>
    <div>
        <input type="radio" value="borrowed" v-model="bookData.ownership">
    </div>
    <div>
        <input type="radio" value="bought" v-model="bookData.ownership">
    </div>
    <button type="submit" name="button"> Add book</button>
</form></template>

<script>
export default {
  name: "BookForm",
  props: ["books"],
  data() {
    return {
    bookData:{
      bookTitle:"",
      bookAuthor:"",
      finishedReading:false,
      ownership:[]
      }
    };
  },
  methods: {
      bookSubmit(bookData){
          this.$emit('add-book',bookData)
      }
  }
};
</script>

<style>
</style>
