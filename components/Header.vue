<template>
  <div id="header" :class="scrolling ? 'scrolling' : ''">
    Header
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'Header',
  data () {
    return {
      scrolling: false
    }
  },
  beforeMount () { window.addEventListener('scroll', this.handleScroll) },
  destroyed () { window.removeEventListener('scroll', this.handleScroll) },
  methods: {
    handleScroll () {
      if (window.scrollY > 50) {
        this.scrolling = true
      } else {
        this.scrolling = false
      }
    },
  }
})
</script>

<style lang="scss" scoped>
#header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 5000;
  transition: background-color .5s;

  &.scrolling { background-color: #fff; }
}
</style>
