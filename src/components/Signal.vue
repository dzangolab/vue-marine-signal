<template>
  <span class="marine-signal">
    <Flag
      :char="char"
      :key="i"
      v-for="(char, i) in chars" />
  </span>
</template>

<script>
import Flag from './SignalFlag'
import '@/assets/scss/marine-signal.scss'

export default {
  components: {
    Flag
  },

  computed: {
    chars () {
      let chars = []
      let clean = this.msg
        .replace(/[^A-Za-z0-9]/g, '')
        .toLowerCase()

      for (var i = 0; i < clean.length; i++) {
        let c = clean.charAt(i)

        if (c !== '') {
          chars.push(c)
        }
      }

      return chars
    }
  },

  name: 'Signal',

  props: {
    msg: {
      type: [Object, String]
    }
  }
}
</script>
