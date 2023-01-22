<template>
  <div class="stats">
    <div class="stats-border stats-right">
      <div class="stats-icon">
        <icon name="star" />
      </div>
      <span>Star</span>
    </div>
    <div class="stats-border">{{ stars }}</div>
    <div class="stats-border">
      <div class="stats-icon">
        <icon name="fork" />
      </div>
      <span>Forks</span>
    </div>
    <div class="stats-border stats-left">{{ forks }}</div>
  </div>
</template>

<script>
import { icon } from '../../icons'
export default {
  components: {
    icon
  },
  props: {
    stars: {
      type: Number,
      required: true
    },
    forks: {
      type: Number,
      required: true
    }
  }
}
</script>

<style lang="scss" src="./stats.scss" scoped></style>
