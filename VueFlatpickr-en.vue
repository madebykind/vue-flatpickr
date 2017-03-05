<template>
  <input type="text" :class="inputClass">
</template>

<script>
import Flatpickr from './assets/flatpickr-en.js'

export default {
  props: {
    options: {
      type: Object
    },
    inputClass: {
      type: String,
    }
  },
  watch: {
    options: {
      handler() {
        this.newFlatpickr()
      },
      deep: true
    }
  },
  ready() {
    new Flatpickr(this.$el, this.options)
  },
  mounted() {
    new Flatpickr(this.$el, this.options)
  }
}
</script>
