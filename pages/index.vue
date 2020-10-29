<template lang="pug">
  v-row
    v-col(cols='12' md='6' lg='4')
      h2.title Hiragana
      p(v-for='a, index in alphabet' :key='index')
        span(v-for='letter, letterIndex in a' :key='letterIndex') {{ letter.Dakuon }}
    v-col(cols='12' md='6' lg='4') Katakana
    v-col(cols='12' md='6' lg='4') Kanji
    ul
      li(v-for='a, key in alphabet' :key="key") {{ key }}
    p {{ katakanaToRomaji }}
</template>

<script>
import { mapState } from 'vuex'
export default {
  data() {
    return {
      katakanaToRomaji: {},
      hiraganaToRomaji: {},
      romajiToHiragana: {},
      romajiToKatakana: {},
      complexRomajiToHiragana: {},
      compleRomajiToKatakana: {},
    }
  },
  computed: {
    ...mapState({
      alphabet: (state) => state.japanese.alphabet,
    }),
  },
  mounted() {
    this.simplestAlphabet(this.alphabet)
    this.SimpleJSON(
      this.alphabet,
      this.complexRomajiToHiragana,
      this.compleRomajiToKatakana
    )
    console.table(this.alphabet.k)
  },
  methods: {
    simplestAlphabet(alphabet) {
      for (const parent in alphabet) {
        if (Object.prototype.hasOwnProperty.call(alphabet, parent)) {
          const vowels = alphabet[parent]

          for (const vowel in vowels) {
            if (Object.prototype.hasOwnProperty.call(vowels, vowel)) {
              const types = vowels[vowel]

              for (const type in types) {
                if (Object.prototype.hasOwnProperty.call(types, type)) {
                  const character = types[type]

                  this.hiraganaToRomaji[character.Hiragana] = character.Romaji
                  this.katakanaToRomaji[character.Katakana] = character.Romaji
                  this.romajiToHiragana[character.Romaji] = character.Hiragana
                  this.romajiToKatakana[character.Romaji] = character.Katakana
                }
              }
            }
          }
        }
      }
    },
    SimpleJSON(alphabet, complexRomajiToHiragana, compleRomajiToKatakana) {
      for (const parent in alphabet) {
        if (Object.prototype.hasOwnProperty.call(alphabet, parent)) {
          const vowels = alphabet[parent]

          complexRomajiToHiragana[parent] = []
          compleRomajiToKatakana[parent] = []

          for (const vowel in vowels) {
            if (Object.prototype.hasOwnProperty.call(vowels, vowel)) {
              const types = vowels[vowel]
              for (const type in types) {
                if (Object.prototype.hasOwnProperty.call(types, type)) {
                  const character = types[type]
                  const tmpHiragana = {}
                  const tmpKatakana = {}

                  tmpHiragana[character.Romaji] = character.Hiragana
                  tmpKatakana[character.Romaji] = character.Katakana

                  complexRomajiToHiragana[parent].push(tmpHiragana)
                  compleRomajiToKatakana[parent].push(tmpKatakana)
                }
              }
            }
          }
        }
      }
    },
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
