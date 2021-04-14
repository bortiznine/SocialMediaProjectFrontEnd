<template>
    <header class="flex">
      <div class="profile-pic">
        <img v-bind:src="post.user.picture ? post.user.picture : defaultPicture"  alt=""/>
      </div>
      <h2 class="username">{{ post.user.username }}</h2>
      <p class="date">Date posted: {{ dateTimeFormatter(post.date) }}</p>
    </header>
</template>

<script>
export default {
  name: 'PostHeader',
  props: {
    defaultPicture: {
      type: String,
      default: "https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png",
    },
    post: Object
  },
  methods: {
    dateTimeFormatter(dateStr) {
      return new Date(dateStr).toLocaleString();
    }
  }
}
</script>


<style scoped>
  header {
    display: flex;
    padding: 20px 0;
    flex-direction: row;
    justify-content: center;
    border-bottom: 1px solid #000;
    background: #EEE;
  }
  header > * {
    margin-right: 20px;
  }
  .profile-pic img {
    width: 80px;
    height: auto;
    display: flex;
    justify-content: inherit;
    align-items: center;
  }
  .username {
    font-weight: 600;
    color: #4d73e8;
    margin: 0 30px;
        display: flex;
    justify-content: inherit;
    align-items: center;
  }
  .date {
    display: flex;
    justify-content: inherit;
    align-items: center;
  }
</style>
