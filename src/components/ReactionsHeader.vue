<template>
    <div class="reactions-flex">
        <div class="reaction like">
            <div class="emoji">👍 Like</div>
            <div class="number">{{post.reactionsCount.like}}</div>
        </div>
        <div class="reaction laugh">
            <div class="emoji">😂 Laugh</div>
            <div class="number">{{post.reactionsCount.laugh}}</div>
        </div>
        <div class="reaction angry">
            <div class="emoji">😠 Angry</div>
            <div class="number">{{post.reactionsCount.angry}}</div>
        </div>
        <div class="reaction sad">
            <div class="emoji">😢 Sad</div>
            <div class="number">{{post.reactionsCount.sad}}</div>
        </div>
    </div>
</template>


<script>


export default {
  name: 'ReactionsHeader',
  props: {
      post: Object
  }
}
</script>

<style scoped>
    .reactions-flex {
        display: flex;
        justify-content: space-around;
      background-color: #4d73e8;
      color: white;
    }
    .emoji {
        font-size: 20px;
    }
    .number {
        display: flex;
        justify-content: center;
        padding-top: 10px;
        font-size: 20px;
    }
</style>
