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
    }
  },

  data () {
    return {
      isPending: false
    }
  },

  methods: {
    handleClick () {
      const originalOnClick = this.createPromise()
      this.isPending = true
      originalOnClick.finally(() => { this.isPending = false })
    },

    createPromise () {
      const promise1 = new Promise((resolve) => {
        setTimeout(resolve, 2000);
      });
      promise1.then(()=>{this.isPending = false})
    }
  }
}
</script>