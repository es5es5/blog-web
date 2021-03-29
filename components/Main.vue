<template>
  <div>
    <main>
      <div class="card_container">
        <div class="card_wrap">
          <Card
            v-for="index in 200"
            :key="index"
            id="card"
            class="card-item"
            title="하이"
            contents="Lorem ipsum dolor sit amet."
            createtime="2020년 09월 19일"
            writerName="김루이"
          />
        </div>
      </div>
    </main>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'

@Component({
  name: 'Main'
})
export default class Main extends Vue {
}
</script>

<style lang="scss" scoped>
.card_container {
  max-width: 1048px;
  margin: 0 auto;
  padding: 12px;
}

.card_wrap {
  display: grid;
  grid-gap: 20px;
  grid-template-columns: repeat(3, 1fr);

  @media (max-width: 1024px) {
    grid-template-columns: repeat(2, 1fr);
  }
  @media (max-width: 500px) {
    grid-template-columns: repeat(1, 1fr);
  }
}
</style>
