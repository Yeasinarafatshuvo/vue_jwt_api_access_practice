<template>
  <h1>{{ title }}</h1>
  <input type="text" v-model="searchTrem" />
  <div v-for="post in filter_search" :key="post.id">
    <h1>{{ post.title }}</h1>
    <p>{{ post.body || snippet }}</p>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      title: "POSTS",
      posts: [],
      searchTrem: "",
    };
  },
  computed: {
    filter_search() {
      return this.posts.filter((post) => {
        return post.title.match(this.searchTrem);
      });
    },
  },
  methods: {},

  created() {
    axios
      .get("https://jsonplaceholder.typicode.com/posts")
      .then((response) => {
        this.posts = response.data;
      })
      .catch((error) => {
        console.log(error);
      });
  },
};
</script>

<style></style>
