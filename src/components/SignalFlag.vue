<template>
  <i :class="cls"></i>
</template>

<script>
import '@/assets/scss/marine-signal.scss'

export default {
  computed: {
    cls () {
      return 'flag-icon flag-icon-' + this.char
    }
  },

  name: 'SignalFlag',

  props: {
    char: {
    }
  }
}
</script>
