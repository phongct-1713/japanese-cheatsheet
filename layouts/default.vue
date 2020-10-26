<template lang="pug">
  v-card.overflow-hidden
    v-app-bar(absolute='' color='white' elevate-on-scroll='' scroll-target='#scrolling-techniques-7')
      v-app-bar-nav-icon
      v-toolbar-title Title
      v-spacer
      v-btn(icon='')
        v-icon mdi-magnify
      v-btn(icon='')
        v-icon mdi-heart
      v-btn(icon='')
        v-icon mdi-dots-vertical
    v-sheet#scrolling-techniques-7.overflow-y-auto(max-height='600')
      v-container(style='height: 1500px;')
        nuxt-link(to='/') Cheatsheet
        nuxt-link.red(to='/memorize') Memorize
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
