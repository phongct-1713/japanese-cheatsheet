<template lang="pug">
  v-sheet
    v-row(v-for='item, index in data' :key='index')
      v-col(cols='12').app-title 『 {{ item.title }} 』
      v-col(cols='12' md='6' lg='4' v-for='section, sectionIndex in item.section' :key='sectionIndex')
        v-row
          v-col(cols='12') {{ section.title }}
          v-col(cols='12')
            p(v-for='letter, letterIndex in section.data' :key='letterIndex') {{ letter.hiragana }}

</template>

<script>
export default {
  data() {
    return {
      data: {
        hiragana: {
          title: 'Hiragana',
          section: {
            alphabet: {
              title: 'Alphabet',
              data: [
                {
                  hiragana: 'あ',
                  romaji: 'a',
                },
                {
                  hiragana: 'い',
                  romaji: 'i',
                },
                {
                  hiragana: 'う',
                  romaji: 'u',
                },
                {
                  hiragana: 'え',
                  romaji: 'e',
                },
                {
                  hiragana: 'お',
                  romaji: 'o',
                },
                {
                  hiragana: 'か',
                  romaji: 'ka',
                },
                {
                  hiragana: 'か',
                  romaji: 'ki',
                },
                {
                  hiragana: 'く',
                  romaji: 'ku',
                },
                {
                  hiragana: 'け',
                  romaji: 'ke',
                },
                {
                  hiragana: 'こ',
                  romaji: 'ko',
                },
              ],
            },
            yoon: {
              title: 'Yoon',
              data: [
                {
                  hiragana: 'きゃ',
                  romaji: 'kya',
                },
                {
                  hiragana: 'きゅ',
                  romaji: 'kyu',
                },
                {
                  hiragana: 'きょ',
                  romaji: 'kyo',
                },
              ],
            },
            dakuon: {
              title: 'Dakuon',
              data: [
                {
                  hiragana: 'か',
                  romaji: 'ga',
                },
                {
                  hiragana: 'ぎ',
                  romaji: 'gi',
                },
                {
                  hiragana: 'ぐ',
                  romaji: 'gu',
                },
                {
                  hiragana: 'げ',
                  romaji: 'ge',
                },
                {
                  hiragana: 'ご',
                  romaji: 'go',
                },
              ],
            },
          },
        },
      },
    }
  },
}
</script>

<style lang="scss" scoped>
ul {
  display: flex;
  width: 100%;
  padding: 0;
  margin: 0;

  li {
    flex: 1;
    list-style: none;
  }
}
</style>
