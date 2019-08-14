<template>
  <div>
    {{ count }}
    <button @click="increment">+</button>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import useCount from '~/compositions/useCount'

export default Vue.extend({
  props: {
    initialCount: {
      type: Number,
      default: 0
    }
  },
  setup(props) {
    return {
      ...useCount(props.initialCount)
    }
  }
})
</script>
