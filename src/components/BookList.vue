<template>
  <div>
    <h1>{{ data().title }}</h1>
  </div>
</template>

<script>
  export default {
    name: 'BookList',
    methods: {
      data: function() {
        return {
          title: "All Books"
        }
      }
    }
  }
</script>

<style>
  h1,
  h2 {
    font-weight: normal;
  }
</style>
