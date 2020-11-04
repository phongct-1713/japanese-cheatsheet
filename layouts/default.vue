<template lang="pug">
  v-container.app
    v-app-bar.app-nav(flat dense)
      v-toolbar-title.app-title {{ title }}
      v-spacer
      v-btn.mr-5(text to='/') Cheatsheet
      v-btn.ml-2(text to='/memorize') Memorize
    transition(transition='scroll-y-transition')
      Nuxt

</template>

<script>
export default {
  data() {
    return {
      title: 'Japanense Cheatsheet',
    }
  },
}
</script>
<style lang="scss">
@import '~assets/scss/layouts/default.scss';
</style>
