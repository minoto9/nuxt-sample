<template>
  <div>
    <hoge :title="indexTitle" >
      <div class="come">
        slot example
      </div>
    </hoge>
    <nuxt-link to="/about">ABOUT</nuxt-link>
  </div>
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