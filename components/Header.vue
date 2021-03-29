<template>
  <div id="header" :class="scrolling ? 'scrolling' : ''">
    <div class="header_wrap">
      <h1 class="heading">Blog</h1>
    </div>
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
  transition: all .5s;

  width: 100%;
  height: 50px;
  background-color: #87c323;
  border-bottom: 1px solid transparent;

  &.scrolling {
    background-color: #fff;
    border-bottom: 1px solid gray;
  }
}

.header_wrap {
  width: 1024px;
  margin: 0 auto;
  color: #fff;
}
</style>
