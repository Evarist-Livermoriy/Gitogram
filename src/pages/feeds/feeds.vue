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
              <icon name="profile" />
            </div>
            <div class="exit">
              <icon name="exit" />
            </div>
          </div>
        </div>
      </template>
      <template #content>
        <ul class="stories">
          <li class="stories-item" v-for="story in stories" :key="story.id">
            <story-user-item :avatar="story.avatar" :username="story.username" />
          </li>
        </ul>
      </template>
    </topline>
  </div>

  <ul class="feeds-list">
    <li class="feeds-item feed" v-for="item in 5" :key="item">
      <feed>
        <template #card>
          <card title="VUE.JS" desc="framework" stars="150" forks="4"/>
        </template>
      </feed>
    </li>
  </ul>
</template>

<script>
import { topline } from '../../components/topline'
import { icon } from '../../icons'
import { storyUserItem } from '../../components/storyUserItem'
import { feed } from '../../components/feed'
import { card } from '../../components/card'
import stories from './data.json'
export default {
  name: 'feeds',
  components: {
    topline,
    icon,
    storyUserItem,
    feed,
    card
  },
  data () {
    return {
      stories
    }
  }
}
</script>

<style lang="scss" src="./feeds.scss" scoped></style>
