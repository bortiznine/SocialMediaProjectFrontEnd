<template>
    <div class="flex-row">
      <h3>{{post.title}}</h3>
      <p class="content">{{post.content}}</p>
    </div>
</template>

<script>
export default {
  name: 'PostBody',
  props: {
    post: Object,
  },
}
</script>


<style scoped>
  article {
    margin: 0 auto;
    width: 600px;
  }
  img {
    width: 50px;
    height: auto;
  }
  .flex-row {
    display: flex;
    flex-direction: column;
    justify-content: center;
    background: #FFF;
    flex: 0 0 50%;
    padding: 1em;
  }
</style>
