<template>
  <div>
    <Header />
    <div class="abc">
      a
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'
import Header from '@/components/Header'

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
