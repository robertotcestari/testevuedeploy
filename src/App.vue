<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Beto Cestari Teste"/> -->
    <h1 class="tw-text-red">Esse é o meu Site do Beto</h1>
    <p
      class="tw-text-grey-darker"
    >Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam deleniti sed iste ad quos iusto hic delectus, repudiandae a enim eligendi magni nihil mollitia, amet dicta ea illum quia voluptates.</p>

    <img src="./assets/img/beto.png" alt>

    <Postsmari/>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Postsmari from "./components/Postsmari.vue";

import Axios from "axios";
Axios.get("https://jsonplaceholder.typicode.com/posts").then(data => {
  console.log(data);
});

export default {
  name: "app",
  components: {
    HelloWorld,
    Postsmari
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
