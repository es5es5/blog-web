<template>
  <div>Hello Blog Web</div>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'

@Component({ middleware ({ redirect }) { return redirect('/main') } })
export default class extends Vue {}
</script>
