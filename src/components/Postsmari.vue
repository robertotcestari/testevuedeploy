<template>
  <div class="hello">
    <div class="tw-my-3" v-for="post in posts">
      <h3 class="tw-text-red">{{ post.title }}</h3>
      <p>{{post.body}}</p>
    </div>

    <p></p>
  </div>
</template>

<script>
import Axios from "axios";
export default {
  name: "Postsmari",
  data: function() {
    return {
      posts: ""
    };
  },

  mounted() {
    Axios.get("https://jsonplaceholder.typicode.com/posts").then(data => {
      this.posts = data.data;
    });
  }
};
</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
