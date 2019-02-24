<template>
<body>
  <div id="app">
    <header class="nav-bar"></header>

    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Lister!"/>
    <h2>Here's a List:</h2>
    <List />
    <Product />
  </div>
</body>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import List from './components/List.vue'
import Product from './components/Product.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    List,
    Product
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Montserrat:400,700');

body {
  background-color: #EEEEEE;
  font-family: 'Montserrat', sans-serif;
  justify-items: center;
  align-items: center;
  text-align: center;
  padding: 0;
  margin: 0;
}

body, html {
  margin: 0;
  height: 100%;
}

h2 {
  text-align: center;
}

.nav-bar {
  background: linear-gradient(-90deg, #84CF6A, #16C0B0);
  height: 60px;
  padding-top: 0;
  margin-bottom: 15px;
  width: 100%;
}
</style>
