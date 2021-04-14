<template>
  <article class="flex-row">
    <div class="profile-pic">
      <img v-bind:src="comment.user.picture ? comment.user.picture : defaultPicture"  alt=""/>
    </div>
    <CommentBody v-bind:comment="comment"/>
  </article>
</template>

<script>
import CommentBody from "@/components/CommentBody";

export default {
  name: 'Comment',
  components: {CommentBody},
  props: {
    comment: Object,
  }
}
</script>

<style scoped>
  .flex-row {
    display: flex;
    flex-direction: row;
  }
  .profile-pic img {
    width: 65px;
    height: auto;
  }
</style>

