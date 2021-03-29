<template>
  <div>
    <Header />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'
import Header from '@/components/Header.vue'

@Component({
  components: {
    Header
  }
})
export default class extends Vue {
  authorName: string = 'JHyeok'
}
</script>

<style lang="scss" scoped>
.abc {
  height: 150vh;
}
</style>
