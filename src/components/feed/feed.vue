<template>
  <div class="feed">
    <div class="feed-user">
      <avatar avatar="https://picsum.photos/200/300" class="feed-avatar"/>
      <div class="feed-username">Username</div>
    </div>

    <div class="feed-card">
      <slot name="card"></slot>
    </div>

    <div class="feed-toggler">
      <toggler @onToggle="showComments" class="toggler"/>
      <ul class="feed-comment-list" v-show="isShownComment">
        <li class="feed-comment-item comment" v-for="item in 5" :key="item">
          <comment username="James" text="Hello" />
        </li>
      </ul>
    </div>

    <div class="feed-date">15 may</div>
  </div>
</template>

<script>
import { avatar } from '../avatar'
import { toggler } from '../toggler'
import { comment } from '../comment'
export default {
  components: {
    avatar,
    toggler,
    comment
  },
  data () {
    return {
      isShownComment: false
    }
  },
  methods: {
    showComments (state) {
      this.isShownComment = state
    }
  }
}
</script>

<style lang="scss" src="./feed.scss" scoped></style>
