<template>
  <div class="card">
    <div class="title-wrap">
      <h2 class="card-title">{{ title }}</h2>
    </div>

    <div class="card-desc-wrap">
      <div class="card-desc">{{ desc }}</div>
    </div>

    <div class="card-stats">
      <stats :stars="stars" :forks="forks"/>
    </div>
  </div>
</template>

<script>
import { stats } from '../stats'
export default {
  components: {
    stats
  },
  props: {
    title: {
      type: String,
      required: true
    },
    desc: {
      type: String,
      required: true
    },
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

<style lang="scss" src="./card.scss" scoped></style>
