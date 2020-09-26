<template>
  <div class="home">
    <h1>Welcome to my website!</h1>
    <p>
      My name is Garrett Rose. I am a self taught web developer from Charlotte,
      North Carolina. I am for hire. 
    </p>
    <img src="../pics/profilePic.jpg" alt="vue logo" /><br />
    <a href="https://github.com/GLRose">Github</a>
  </div>
</template>

<script>
export default {
  name: "Home",
  props: {
    msg: String,
  },
  components: {
      
  }
};

const axios = require("axios")

axios.post("http://localhost:8080/", {
  title: "foo",
  body: "bar",
  userId: 1
}).then(function(response) {
  console.log(response.data)
}).catch(function(error) {
  console.log(error)
})
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

img {
  border: 10px solid #555;
}

form {
  margin-top: 20px;
}
</style>
