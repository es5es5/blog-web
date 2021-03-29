<template>
  <div>
    <div class="thumbnail_wrap">
      <span>{{ title }}</span>
      <!-- <img :src="imgUrl" alt="image"> -->
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'
@Component({
  name: 'Card'
})
export default class Card extends Vue {
  title: string = '흥미로운 이야기'
  contents: string = 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam assumenda harum veritatis eum autem quis mollitia dolorem iure voluptatum cum.'
  writerName: string = '김루이'
  imgUrl: string = ''
}
</script>

<style lang="scss" scoped>

</style>
