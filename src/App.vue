<template>
  <div id="app">
    <Todolist />
  </div>
</template>

<script>
  import Todolist from './components/Todolist.vue';
  export default {
    name: 'App',
    components: {
      Todolist,
    },
  };
</script>

<style>
  @import 'https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;700&display=swap';

  * {
    margin: 0;
    padding: 0;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
    line-height: 1.6;
  }

  *:before,
  *:after {
    margin: 0;
    padding: 0;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
    line-height: 1.6;
  }

  html {
    scroll-behavior: smooth;
  }

  body,
  html {
    height: 100%;
    padding-top: 0;
    width: 100%;
    font-family: 'Open Sans', sans-serif;
  }
</style>
