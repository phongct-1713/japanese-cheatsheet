<template lang="pug">
  v-sheet.app-content
    v-row(v-for='item, index in data' :key='index')
      v-col(cols='12').section-title 『 {{ item.title }} 』
        span {{ item.subTitle}} Cheatsheet
      v-col(cols='12' md='6' lg='4' v-for='section, sectionIndex in item.section' :key='sectionIndex')
        v-row
          v-col.section-sub-title(cols='12') 「 {{ section.title }} 」
            span {{ section.subTitle }}
          v-col(cols='12')
            .app-box
              .app-box__des
                p {{ section.des }}
              .app-box__section
                p(v-for='letter, letterIndex in section.data' :key='letterIndex') {{ letter.hiragana }}

</template>

<script>
export default {
  data() {
    return {
      data: {
        hiragana: {
          title: 'ひらがな',
          subTitle: 'hiragana',
          section: {
            alphabet: {
              title: '五十音',
              subTitle: 'Gojūon',
              des:
                'In Japanese, syllables are organized in the form of a table (5 x 10). This table is called gojūon-zu (literally means table of 50 sounds).',
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
                {
                  hiragana: 'さ',
                  romaji: 'sa',
                },
                {
                  hiragana: 'し',
                  romaji: 'shi',
                },
                {
                  hiragana: 'す',
                  romaji: 'su',
                },
                {
                  hiragana: 'せ',
                  romaji: 'se',
                },
                {
                  hiragana: 'そ',
                  romaji: 'so',
                },
                {
                  hiragana: 'た',
                  romaji: 'ta',
                },
                {
                  hiragana: 'ち',
                  romaji: 'chi',
                },
                {
                  hiragana: 'つ',
                  romaji: 'tsu',
                },
                {
                  hiragana: 'て',
                  romaji: 'te',
                },
                {
                  hiragana: 'と',
                  romaji: 'to',
                },
                {
                  hiragana: 'な',
                  romaji: 'na',
                },
                {
                  hiragana: 'に',
                  romaji: 'ni',
                },
                {
                  hiragana: 'ぬ',
                  romaji: 'nu',
                },
                {
                  hiragana: 'ね',
                  romaji: 'ne',
                },
                {
                  hiragana: 'の',
                  romaji: 'no',
                },
                {
                  hiragana: 'は',
                  romaji: 'ha',
                },
                {
                  hiragana: 'ひ',
                  romaji: 'hi',
                },
                {
                  hiragana: 'ふ',
                  romaji: 'hu',
                },
                {
                  hiragana: 'へ',
                  romaji: 'he',
                },
                {
                  hiragana: 'ほ',
                  romaji: 'ho',
                },
                {
                  hiragana: 'ま',
                  romaji: 'ma',
                },
                {
                  hiragana: 'み',
                  romaji: 'mi',
                },
                {
                  hiragana: 'む',
                  romaji: 'mu',
                },
                {
                  hiragana: 'め',
                  romaji: 'me',
                },
                {
                  hiragana: 'も',
                  romaji: 'mo',
                },
                {
                  hiragana: 'や',
                  romaji: 'ya',
                },
                {
                  hiragana: '（い）',
                  romaji: 'i',
                },
                {
                  hiragana: 'ゆ',
                  romaji: 'yu',
                },
                {
                  hiragana: '（え）',
                  romaji: 'e',
                },
                {
                  hiragana: 'よ',
                  romaji: 'yo',
                },
                {
                  hiragana: 'ら',
                  romaji: 'ra',
                },
                {
                  hiragana: 'り',
                  romaji: 'ri',
                },
                {
                  hiragana: 'る',
                  romaji: 'ru',
                },
                {
                  hiragana: 'れ',
                  romaji: 're',
                },
                {
                  hiragana: 'ろ',
                  romaji: 'ro',
                },
                {
                  hiragana: 'わ',
                  romaji: 'wa',
                },
                {
                  hiragana: '（い）',
                  romaji: 'i',
                },
                {
                  hiragana: '（う）',
                  romaji: 'u',
                },
                {
                  hiragana: '（え）',
                  romaji: 'e',
                },
                {
                  hiragana: 'を',
                  romaji: 'wo',
                },
                {
                  hiragana: 'ん',
                  romaji: 'n',
                },
              ],
            },
            yoon: {
              title: '拗音',
              subTitle: 'Yōon',
              des:
                'Yōon is a combination of the consonant of i-column syllables and ya, yu or yo. For example, k + ya = kya.',
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
                {
                  hiragana: '',
                  romaji: '',
                },
                {
                  hiragana: '',
                  romaji: '',
                },
                {
                  hiragana: 'しゃ',
                  romaji: 'sha',
                },
                {
                  hiragana: 'しゅ',
                  romaji: 'shu',
                },
                {
                  hiragana: 'しょ',
                  romaji: 'sho',
                },
                {
                  hiragana: '',
                  romaji: '',
                },
                {
                  hiragana: '',
                  romaji: '',
                },
                {
                  hiragana: 'ちゃ',
                  romaji: 'cha',
                },
                {
                  hiragana: 'ちゅ',
                  romaji: 'chu',
                },
                {
                  hiragana: 'ちょ',
                  romaji: 'cho',
                },
                {
                  hiragana: '',
                  romaji: '',
                },
                {
                  hiragana: '',
                  romaji: '',
                },
                {
                  hiragana: 'にゃ',
                  romaji: 'nya',
                },
                {
                  hiragana: 'にゅ',
                  romaji: 'nyu',
                },
                {
                  hiragana: 'にょ',
                  romaji: 'nyo',
                },
                {
                  hiragana: '',
                  romaji: '',
                },
                {
                  hiragana: '',
                  romaji: '',
                },
                {
                  hiragana: 'ひゃ',
                  romaji: 'hya',
                },
                {
                  hiragana: 'ひゅ',
                  romaji: 'hyu',
                },
                {
                  hiragana: 'ひょ',
                  romaji: 'hyo',
                },
                {
                  hiragana: '',
                  romaji: '',
                },
                {
                  hiragana: '',
                  romaji: '',
                },
                {
                  hiragana: 'びゃ',
                  romaji: 'bya',
                },
                {
                  hiragana: 'びゅ',
                  romaji: 'byu',
                },
                {
                  hiragana: 'びょ',
                  romaji: 'byo',
                },
                {
                  hiragana: '',
                  romaji: '',
                },
                {
                  hiragana: '',
                  romaji: '',
                },
                {
                  hiragana: 'ぴゃ',
                  romaji: 'pya',
                },
                {
                  hiragana: 'ぴゅ',
                  romaji: 'pyu',
                },
                {
                  hiragana: 'ぴょ',
                  romaji: 'pyo',
                },
              ],
            },
            dakuon: {
              title: '濁音',
              subTitle: 'Dakuon',
              des:
                'Dakuon literally means turbid or murky sound. It is the voiced sound of か [ka], さ [sa], た [ta] and は [ha]-row syllables.',
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
                {
                  hiragana: 'ざ',
                  romaji: 'za',
                },
                {
                  hiragana: 'し',
                  romaji: 'shi',
                },
                {
                  hiragana: 'ず',
                  romaji: 'zu',
                },
                {
                  hiragana: 'ぜ',
                  romaji: 'ze',
                },
                {
                  hiragana: 'ぞ',
                  romaji: 'zo',
                },
                {
                  hiragana: 'だ',
                  romaji: 'da',
                },
                {
                  hiragana: 'ぢ',
                  romaji: 'ji',
                },
                {
                  hiragana: 'づ',
                  romaji: 'zu',
                },
                {
                  hiragana: 'で',
                  romaji: 'de',
                },
                {
                  hiragana: 'ど',
                  romaji: 'do',
                },
                {
                  hiragana: 'ば',
                  romaji: 'ba',
                },
                {
                  hiragana: 'び',
                  romaji: 'bi',
                },
                {
                  hiragana: 'ぶ',
                  romaji: 'bu',
                },
                {
                  hiragana: 'べ',
                  romaji: 'be',
                },
                {
                  hiragana: 'ぼ',
                  romaji: 'bo',
                },
              ],
            },
            handakuon: {
              title: '半濁音',
              subTitle: 'Handakuon',
              des: 'Handakuon literally means half-turbid or half-murky sound.',
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
