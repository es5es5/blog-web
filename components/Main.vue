<template>
  <div>
    <main>
      <Card
        id="card"
        title="하이"
        contents="헬로우"
      />
    </main>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'

@Component({
})
export default class Main extends Vue {
  abc: string = 'P'
  get _abc (): string { return this.abc }
}
</script>

<style lang="scss" scoped>
</style>
