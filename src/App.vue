<template>
  <div id="app">
    <ul>
      <!-- <li><router-link to="/">Home</router-link></li>
      <li><router-link to="about">About</router-link></li> -->
    </ul>
    <router-view />
  </div>
</template>

<script>
//registering our components so we can embed them like "<> </>"
export default {

};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

ul {
  list-style-type: none;
  width: auto;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333;
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 18px 18px;
  text-decoration: none;
}

/* Change the link color to #111 (black) on hover */
li a:hover {
  background-color: #111;
}
</style>
