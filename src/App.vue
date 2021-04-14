<template>
 <div>
  <Title :title="title"/>
  <Posts class="all-posts" :posts="posts" />
 </div>
</template>

<script>
import Posts from "@/components/Posts";
import Title from "@/components/Title";

export default {
  name: 'App',
  components: {
    Posts, Title
  },
  data() {
    return {
      posts: [],
    }
  },
  async created() {
    this.posts = await this.fetchPosts()
  },
  methods: {
    async fetchPosts() {
      const res = await fetch('http://localhost:9092/api/posts')
      return await res.json()
    },
  }
}
</script>

<style>
body, html {
  padding: 0;
  margin: 0;
  width: 100%;
  min-height: 100%;
  background-color: rgb(235, 235, 235);
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1 {
  font-size: 2.8em;
}

h2 {
  font-size: 2.2em;
}

h3 {
  font-size: 1.6em;
}

  .comment:nth-child(odd) {
      background: #a6ccf7;
  }
  .comment:nth-child(even) {
      background: #6299d8;
  }
</style>
