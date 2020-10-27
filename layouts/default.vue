<template lang="pug">
  v-container
    v-app-bar(flat dense)
      v-toolbar-title {{ title }}
      v-btn(to='/') Cheatsheet
      v-btn(to='/memorize') Memorize
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
