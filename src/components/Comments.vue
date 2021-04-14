<template>
   <div>
      <div class="comment" v-bind:key="comment.id" v-for="comment in comments">
        <Comment v-bind:comment="comment" />
      </div>
  </div>
</template>


<script>
import Comment from "@/components/Comment"

export default {
  name: 'Comments',
  props: {
    comments: Array,
  },
  components: {
    Comment,
  },

}
</script>

<style>

</style>