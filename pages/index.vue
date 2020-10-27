<template lang="pug">
  v-row
    v-col(cols='12' md='6' lg='4')
      h2.title Hiragana
    v-col(cols='12' md='6' lg='4') Katakana
    v-col(cols='12' md='6' lg='4') Kanji
</template>

<script>
import { mapState } from 'vuex'
export default {
  computed: {
    ...mapState({
      state: (state) => state,
    }),
  },
  mounted() {
    console.log(this.state)
  },
}
</script>
