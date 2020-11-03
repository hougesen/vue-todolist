<template>
  <div id="app">
    <nav>
      <router-link to="/">Home</router-link>
    </nav>
    <router-view />
  </div>
</template>

<script>
  export default {
    name: 'App',
    components: {},
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
  body {
    width: 50%;
    margin: auto;
  }

  nav {
    padding: 20px 20px 20px 0;
  }
  nav a {
    padding: 10px;
    text-decoration: none;
    background: #fff;
    border-radius: 3px;
    color: rgb(0, 110, 255);
    font-weight: bold;
    margin-right: 15px;
  }
</style>
