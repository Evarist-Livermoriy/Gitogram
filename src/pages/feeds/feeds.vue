<template>
  <div class="topline">
    <topline>
      <template #headline>
        <div class="header">
          <div class="title">
            <h1>Gitogram /</h1>
          </div>
          <div class="icons">
            <div class="home">
              <icon name="home" />
            </div>
            <div class="profile">
              <img src="../../../../img/Photo.png" />
            </div>
            <div class="shape">
              <icon name="shape" />
            </div>
          </div>
        </div>
      </template>
      <template #content>
        <ul class="stories">
          <li class="stories-item" v-for="story in stories" :key="story.id">
            <story-user-item :avatar="story.avatar" :username="story.username" @onPress="handlePress" />
          </li>
        </ul>
      </template>
    </topline>
  </div>
  <toggler />
</template>

<script>
import { topline } from '../../components/topline'
import { icon } from '../../icons'
import { storyUserItem } from '../../components/storyUserItem'
import { toggler } from '../../components/toggler'
import stories from './data.json'
export default {
  name: 'feeds',
  components: {
    topline,
    icon,
    storyUserItem,
    toggler
  },
  data () {
    return {
      stories
    }
  }
}
</script>

<style lang="scss" src="./feeds.scss" scoped></style>
