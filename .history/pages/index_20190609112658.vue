<template>
  <hoge :title="indexTitle" >
    <div class="come">
      slot example
    </div>
  </hoge>
</template>

<script>
import Hoge from '~/components/Hoge.vue'

export default {
  components: {
    Hoge
  },
  data() {
    return {
      indexTitle: 'Nuxt.js data'
    }
  }
}
</script>

<style>
</style>