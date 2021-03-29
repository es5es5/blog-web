<template>
  <div>
    <main>
      {{ _abc }}
    </main>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'

@Component({
  name: 'Main',
})
export default class Main extends Vue {
  abc: string = 'P'
  get _abc (): string {
    return this.abc
  }
}
</script>

<style lang="scss" scoped>
</style>
