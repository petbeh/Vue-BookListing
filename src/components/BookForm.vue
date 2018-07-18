<template>
  <form class="" action="#" method="post">
    <input v-model="bookTitle" type="text" name="title" value="" placeholder="Book Title">
    <input v-model="bookAuthor" type="text" name="author" value="" placeholder="Book Author">
    <button @submit.prevent="bookSubmit(bookTitle, bookAuthor)" type="submit" name="button">Add Book</button>
  </form>
</template>

<script>
export default {
  name: 'BookForm',
  props: [ 'books' ],
  data: function() {
    return {
      bookTitle: '',
      bookAuthor: ''
    }
  },
  methods: {
    bookSubmit: function(bookTitle, bookAuthor) {
      this.$emit('addBook', bookTitle, bookAuthor);
    }
  }
}
</script>

<style>
h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}
</style>
