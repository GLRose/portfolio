<template>
  <div class="home">
    {{ pokemon }}
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
import axios from "axios";

export default {
  name: "Home",
  props: {
    msg: String,
  },
  data() {
    return {
      pokemon: {},
    };
  },
  created() {
    axios
      .get("https://pokeapi.co/api/v2/pokedex/kanto/")
      .then((response) => {
        console.log(response);
        for (var x = 0; x < response.data.pokemon_entries.length; x++) {
          this.pokemon = response.data.pokemon_entries[x].pokemon_species.name;
          // console.log(response.data.pokemon_entries[x].pokemon_species.name)
        }
      })
      .catch((err) => {
        console.log(err);
      });
  },
};
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
  border: 5px solid #555;
}
</style>
