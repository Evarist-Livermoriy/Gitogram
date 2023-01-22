<template>
  <button class="button " :class="{ 'active': isOpened }" @click="onToggle">
    <span class="text">{{isOpened ? 'Hide' : 'Show'}} issues</span>
    <span class="icon">
      <icon name="triangle" />
    </span>
  </button>
</template>

<script>
import { icon } from '../../icons'

export default {
  components: {
    icon
  },
  data () {
    return {
      isOpened: false
    }
  },
  emits: [
    'onToggle'
  ],
  methods: {
    onToggle () {
      this.isOpened = !this.isOpened
      this.$emit('onToggle', this.isOpened)
    }
  }
}
</script>

<style lang="scss" src="./toggler.scss" scoped></style>
