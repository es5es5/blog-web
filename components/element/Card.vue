<template>
  <div :id="id" class="card-item">
    <div class="thumnail_wrap" />
    <div class="title_wrap">
      <p class="title">{{ title }}</p>
    </div>
    <div class="contents_wrap">
      <p class="contents">{{ contents }}</p>
    </div>
    <div class="createtime_wrap">
      <p class="createtime">{{ createtime }} · 조회 152 · 댓글 10</p>
    </div>
    <div class="writer_wrap">
      <p class="writerName">{{ writerName }}</p>
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

  @Prop({ type: String, default: '1999-01-01', required: true })
  readonly createtime!: string

  @Prop({ type: String, default: '', required: false })
  readonly imgUrl!: string
}
</script>

<style lang="scss" scoped>
@mixin card {
  padding: 10px;
}

.card-item {
  justify-content: center;
  align-items: center;

  background-color: #fff;
  border-radius: 6px;
  box-shadow: 0px 0px 50px 15px rgba(187, 187, 187, .1);
  -webkit-box-shadow: 0px 0px 50px 15px rgba(187, 187, 187, .1);
  -moz-box-shadow: 0px 0px 50px 15px rgba(187, 187, 187, .1);
  transition: box-shadow, transform 0.25s ease-in 0s, transform 0.25s ease-in 0s;

  font-size: 16px;

  @media (max-width: 1024px) { font-size: 18px; }
  @media (max-width: 750px) { font-size: 20px; }

  &:hover {
    cursor: pointer;
    box-shadow: 0px 0px 50px 15px rgba(187, 187, 187, .2);
    -webkit-box-shadow: 0px 0px 50px 15px rgba(187, 187, 187, .2);
    -moz-box-shadow: 0px 0px 50px 15px rgba(187, 187, 187, .2);
    transform: translatey(-8px);
  }
}

.thumnail_wrap {
  height: 10em;
  border-radius: 6px 6px 0 0;
  background-color: rgba(deepskyblue, .3);
}

.title_wrap {
  @include card;
  font-weight: bold;
  font-size: 1.2em;
}

.contents_wrap {
  @include card;
  font-size: 1em;
  min-height: 8em;
}

.createtime_wrap {
  @include card;
  display: flex;
  color: #868E96;
  font-size: .8em;
}

.writer_wrap {
  @include card;
  display: flex;
  font-weight: bold;
  font-size: .8em;
}
</style>
