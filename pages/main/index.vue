<template>
  <div>
    <Header />
    <div class="main_wrap">
      <router-view />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'
import Header from '@/components/Header.vue'

@Component({
  components: {
    Header,
  }
})
export default class extends Vue {
}
</script>

<style lang="scss" scoped>
.main_wrap {
  margin-top: 100px;
}
</style>
