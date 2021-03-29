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
      if (window.scrollY > 10) {
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
  transition: all .3s;

  width: 100%;
  height: 60px;
  color: #87c323;
  background-color: rgba(#fff, .1);
  border-bottom: 1px solid rgba(gray, .25);

  &.scrolling {
    background-color: #87c323;
    border-bottom: 1px solid transparent;
    color: #fff;
  }
}

.header_wrap {
  width: 1084px;
  padding: 0 30px;
  margin: 0 auto;
}

.heading {
  vertical-align: middle;
  line-height: 55px;
  font-size: 30px;
  font-weight: bold;
}
</style>
