<template>
    <div class="flex-column">
      <p class="username">{{comment.user.username}}</p>
      <p class="content">{{comment.text}}</p>
      <p class="date">{{ dateTimeFormatter(comment.date) }}</p>
    </div>
</template>

<script>
export default {
  name: 'CommentBody',
  props: {
    comment: Object,
  },
  methods: {
    dateTimeFormatter(dateStr) {
      return new Date(dateStr).toLocaleString();
    }
  }
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
  p {
    margin: 0;
  }
  .date {
    font-size: 0.75em;
    margin-top: 5px;
  }
  .flex-column {
    display: flex;
    flex-direction: column;
    justify-content: center;
    flex: 0 0 50%;
    padding: 1em;
  }
  .username {
    color: #000;
    font-weight: 600;
  }
</style>
