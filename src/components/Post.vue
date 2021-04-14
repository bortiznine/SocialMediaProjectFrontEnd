<template>
  <article>
    <PostHeader v-bind:post="post"/>
    <PostBody v-bind:post="post"/>
    <Comments v-bind:comments="post.comments"/>
  </article>
</template>

<script>
import PostHeader from "@/components/PostHeader";
import PostBody from "@/components/PostBody";
import Comments from "@/components/Comments";

export default {
  name: 'Post',
  components: {PostHeader, PostBody, Comments},
  props: {
    post: Object,
  }
}
</script>

<style scoped>
  article {
    margin: 0 auto;
    width: 650px;
  }
</style>

<style scoped>
  article {
    border: 1px solid rgb(39, 39, 39);
    margin-bottom: 5em;
  }
</style>