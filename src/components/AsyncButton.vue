<template>
  <base-button
      :disabled="isPending"
      :color="color"
      @click.stop.prevent="handleClick"
  >
    <p v-if="isPending" style="margin: 0">
      Patientez
    </p>
    <slot />
  </base-button>
</template>

<script>
import BaseButton from './BaseButton.vue'

export default {
  name: 'AsyncButton',
  components: { BaseButton },
  inheritAttrs: false,

  props: {
    color: {
      type: String,
      default: 'primary'
    },
    onClick : Function
  },

  data () {
    return {
      isPending: false,
    }
  },

  methods: {
    handleClick () {
      this.isPending = true
      this.onClick().finally(() => { this.isPending = false })
    }
  }
}
</script>