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
    defaultPicture: {
      type: String,
      default: "https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png",
    },
  }
}
</script>

<style scoped>
  .flex-row {
    display: flex;
    flex-direction: row;
  }
  .profile-pic {
    display: flex;
    justify-content: inherit;
    align-items: center;
  }
  .profile-pic img {
    width: 100px;
    height: auto;
  }
</style>

