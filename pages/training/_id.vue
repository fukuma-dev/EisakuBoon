<template>
  <div>
    <div v-if="!isStart">
      <v-btn
        @click="
          start()
          jpSpeech(phrase[num].jp)
        "
      >
        開始しますか？
      </v-btn>
    </div>
    <div v-if="isStart">
      <p>{{ phrase[num].jp }}</p>
      <v-btn
        v-if="!isAnswer"
        @click="
          toAnswer()
          enSpeech(phrase[num].en)
        "
      >
        答え
      </v-btn>
      <div v-if="isAnswer">
        <p>{{ phrase[num].en }}</p>
        <v-btn
          @click="
            next()
            jpSpeech(phrase[num].jp)
          "
        >
          次へ
        </v-btn>
      </div>
    </div>
  </div>
</template>
<script>
import eikaiwa from '~/assets/json/eikaiwa.json'

export default {
  data() {
    return {
      num: 0,
      isStart: false,
      isAnswer: false,
      phrase: eikaiwa
    }
  },
  methods: {
    start() {
      this.isStart = true
    },
    next() {
      this.isAnswer = false
      this.num = this.num + 1
    },
    toAnswer() {
      this.isAnswer = true
    },
    jpSpeech(jpText) {
      const ssu = new SpeechSynthesisUtterance()
      ssu.text = jpText
      ssu.lang = 'ja-JP'
      speechSynthesis.speak(ssu)
    },
    enSpeech(enText) {
      const ssu = new SpeechSynthesisUtterance()
      ssu.text = enText
      ssu.lang = 'en-US'
      speechSynthesis.speak(ssu)
    }
  }
}
</script>
