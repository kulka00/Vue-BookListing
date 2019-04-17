<template>
  <div>
    <h1>{{title}}</h1>
    <ul>
    <li v-for="book in books">
     {{book.title}}:{{book.author}}
    </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'BookList',
  data() {
    return {
      title: 'All Books',
      books:[{title: 'self-Reliance',auther: 'Ralph Waldo Emerson'},
      {title: 'American Gods',auther: 'Neil Geiman'},
      {title: 'Amusing ourselves to Death',auther: 'Neil Postman'}]
    }
  }
}
</script>

<style>
h1,
h2 {
  font-weight: normal;
}
ul{
    list-style-type: none;
    padding: 0
}
</style>
