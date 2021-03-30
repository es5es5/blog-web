<template>
  <div>
    <main id="CardDetail">
      <section>
        <h2 class="title">{{ title }}</h2>
        <p v-html="contents" class="contents" />
      </section>
    </main>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'

@Component({
  name: 'CardDetail'
})
export default class CardDetail extends Vue {
  title: string = '안녕하세요 김루이입니다.'
  contents: string = '<strong> Lorem ipsum dolor sit</strong> amet consectetur adipisicing elit.'
}
</script>

<style lang="scss" scoped>
#CardDetail {
  width: 1024px;
  margin: 0 auto;
}

.title {
  font-size: 35px;
  font-weight: bold;
  margin: 0;
  padding: 20px 0;
}

.contents {
  font-size: 20px;
}
</style>
