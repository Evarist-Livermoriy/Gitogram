<template>
  <div class="comment">
    <div class="comment-username">{{ username }}</div>
    <div class="comment-text">{{ text }}</div>
  </div>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      required: true
    },
    username: {
      type: String,
      required: true
    }
  }
}
</script>

<style lang="scss" src="./comment.scss" scoped></style>
