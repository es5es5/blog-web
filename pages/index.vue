<template>
  <div>
    <Header />
    <div class="main_wrap">
      <Main />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'
import Header from '@/components/Header.vue'
import Main from '@/components/Main.vue'

@Component({
  components: {
    Header,
    Main,
  }
})
export default class extends Vue {
}
</script>

<style lang="scss" scoped>
.main_wrap {
  margin-top: 50px;
}
</style>
