<template>
  <div>
    <main id="CardDetail">
      <section>
        <h2 class="title">{{ title }}</h2>
        <span class="writerName">{{ writerName }}</span><span class="separator"> · </span><span class="createtime">{{ createtime }}</span>
        <ul class="tag_wrap">
          <li class="tag-item">Hello</li>
        </ul>
        <div class="contents_wrap">
          <p v-html="contents" />
        </div>
      </section>
    </main>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'

@Component({
  name: 'CardDetail',
  created () {
    // window.scrollTo({ top: 0 })
    this.$Progress.start()
    setTimeout(() => {
      this.$Progress.finish()
    }, 1000)
  }
})
export default class CardDetail extends Vue {
  title: string = '안녕하세요 김루이입니다.'
  writerName: string = '김루이'
  createtime: string = '2020년 09월 19일'
  views: string = '24'
  contents: string = '<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum ipsum vitae iste sint dolores minima culpa velit, porro alias error itaque voluptate debitis doloremque quasi, rerum excepturi ullam vel commodi.</p><p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Perferendis aliquam quod soluta tempora, magnam ullam vel non minus veritatis veniam?</p><br><p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi nobis quisquam eveniet placeat quod corrupti ut natus asperiores quasi, distinctio dolore culpa quaerat nostrum, aliquid illo velit quos enim! Provident sit blanditiis quae esse, molestias mollitia iure? Animi, quisquam. Recusandae placeat quasi quos veniam enim suscipit porro perspiciatis? Aut beatae neque, ad esse nostrum, incidunt soluta, quis vero quia facilis autem. Dolor repellat magnam molestiae illum aliquam soluta veritatis in atque, quos nulla ea commodi tenetur, eaque eius iusto sequi. Distinctio eius natus veniam ipsum laudantium ipsam totam quis iusto! Debitis itaque a perferendis labore reprehenderit tenetur illo nobis similique nesciunt porro sapiente repudiandae, nemo amet odio at quas est saepe rerum, repellat aliquid pariatur dolores, sunt provident id? Voluptas maxime, numquam sequi voluptatibus sed nulla, reprehenderit debitis dolore error accusamus inventore est obcaecati tempore modi neque dicta. Obcaecati ea esse fuga maiores alias labore error temporibus ipsam distinctio, eaque magni dolorum culpa ipsum hic assumenda quam minus, dicta consequuntur sunt placeat! Eveniet tempora hic necessitatibus animi consectetur, asperiores veritatis reprehenderit nisi corrupti illo dolorem dignissimos nobis modi inventore provident voluptatum expedita accusantium? Velit dolore fuga asperiores numquam impedit beatae quas sed architecto reprehenderit, similique explicabo doloremque amet fugiat ut repellendus quod consequatur corporis cumque earum nulla adipisci? Earum similique provident magni mollitia ab ad aperiam nemo quaerat? Voluptate reiciendis sit tenetur debitis unde necessitatibus, sapiente quas odit. Atque eum ipsa ipsam tenetur reiciendis doloribus, quis aliquam beatae obcaecati voluptate, repudiandae suscipit recusandae explicabo molestias? Aspernatur eum incidunt tempore nisi harum est facilis magni laborum totam laboriosam ratione, non temporibus sapiente ab ipsum doloremque beatae suscipit quidem qui reiciendis ad molestiae debitis. Ea, culpa. Esse voluptates perspiciatis exercitationem nemo optio repudiandae temporibus modi dignissimos, libero at quas, ullam tempora doloremque reiciendis possimus. Facere magni vel soluta similique velit obcaecati quod nesciunt veniam voluptatem quia harum distinctio culpa error nostrum esse, asperiores alias incidunt aliquam odit. Impedit, nam ducimus enim vel beatae quam ratione omnis neque voluptatum? Itaque ipsa sed corporis quidem provident nihil ab cum, aspernatur veritatis magnam nam voluptatem aut alias dolorem explicabo? Nostrum aliquam vitae reiciendis voluptate libero numquam facilis aspernatur expedita labore soluta explicabo autem, modi in cupiditate! Nihil laboriosam expedita libero explicabo quis, placeat velit possimus at soluta, quos corporis laudantium, rem quasi eius. Deserunt, officia reprehenderit dolorum dolores repellat veritatis. At ipsa pariatur officia exercitationem aliquid consequuntur sed iure soluta. Exercitationem consequuntur pariatur natus deleniti!</p>'
}
</script>

<style lang="scss" scoped>
#CardDetail {
  max-width: 1084px;
  padding: 0 30px;
  margin: 0 auto;

  font-size: 20px;

  @media (max-width: 1024px) { font-size: 18px; }
  @media (max-width: 750px) { font-size: 16px; }
}

.title {
  font-size: 2.25em;
  font-weight: bold;
  padding: 1em 0;
}

.writerName {
  font-size: 1.1em;
  font-weight: bold;
}

.createtime {
  font-size: 1.1em;
  font-weight: normal;
  color: #868E96;
}

.contents_wrap {
  padding: 4em 0;
  font-size: 1em;
}
</style>
