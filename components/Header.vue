<template>
  <div id="header" :class="scrolling ? 'scrolling' : ''">
    <div class="header_wrap">
      <nuxt-link tag="h1" :to="{ name: 'index' }" class="heading">Blog</nuxt-link>
      <!-- <nuxt-link tag="button" :to="{ name: 'login' }" class="btn login">로그인</nuxt-link> -->
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
    handleScroll () { this.scrolling = window.scrollY > 10 },
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
    background-color: rgba(#87c323, .95);
    border-bottom: 1px solid transparent;
    color: #fff;
  }
}

.header_wrap {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  max-width: 1084px;
  padding: 0 30px;
  margin: 0 auto;
}

.heading {
  display: inline-block;
  line-height: 60px;
  font-size: 30px;
  font-weight: bold;

  &:hover { cursor: pointer; }
}

.login {
}
</style>
