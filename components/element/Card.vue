<template>
  <div :id="id" class="card-item">
    <div class="title_wrap">
      <p class="title">{{ title }}</p>
    </div>
    <div class="contents_wrap">
      <p class="contents">{{ contents }}</p>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'nuxt-property-decorator'
@Component({
  name: 'Card'
})
export default class Card extends Vue {
  @Prop({ type: String, default: 'card', required: false })
  readonly id!: string

  @Prop({ type: String, default: '흥미로운 이야기', required: true })
  readonly title!: string

  @Prop({ type: String, default: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.', required: false })
  readonly contents!: string

  @Prop({ type: String, default: '김루이', required: true })
  readonly writerName!: string

  @Prop({ type: String, default: '', required: false })
  readonly imgUrl!: string
}
</script>

<style lang="scss" scoped>
.card-item {
  justify-content: center;
  align-items: center;
}
</style>
