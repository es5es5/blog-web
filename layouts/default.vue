<template>
  <div>
    <Nuxt />
    <no-ssr>
      <vue-progress-bar />
    </no-ssr>
  </div>
</template>

<script>
export default {
  head () {
    return {
      title: 'Blog',
      meta: [
        {
          name: 'Blog',
          content: 'My Blog'
        }
      ]
    }
  }
}
</script>

<style>
html {
  font-family:
    'Noto Sans KR',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

body {
  background-color: #F8F9FA;
  min-height: 100vh;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

ul, li {
  margin: 0;
  padding: 0;
  list-style: none;
}
</style>
