<template>
  <input type="text" :class="inputClass">
</template>

<script>
import Flatpickr from 'flatpickr'

export default {
  props: {
    options: {
      type: Object
    },
    inputClass: {
      type: String,
    }
  },
  data() {
    return {
      flatpickr: null,
    };
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
    this.flatpickr = new Flatpickr(this.$el, this.options);
  },
  mounted() {
    this.flatpickr = new Flatpickr(this.$el, this.options);
  }
}
</script>
