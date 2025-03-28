<template>
  <h2 class="heading">I am a a Vue component</h2>
  <h2 class="heading">{{ message }}</h2>
  <h2 class="heading">{{ reversedMessage }}</h2>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
export default defineComponent({
  name: 'MyFirstComponent',
  data() {
    return {
      message: 'Hello World!',
      reversedMessage: 'Hello World!'.split('').reverse().join(''),
    }
  },
  watch: {
    message: function (newVal) {
      this.reversedMessage = newVal.split('').reverse().join('')
    },
  },
  mounted() {
    console.log('Component mounted')
  },
})
</script>
