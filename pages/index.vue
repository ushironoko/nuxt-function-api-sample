<template>
  <div class="container">
    <div>
      <h1>Nuxt + vue-function-api</h1>
      <div>{{ `x: ${x}` }}</div>
      <div>{{ `y: ${y}` }}</div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import useMouse from '~/compositions/useMouse'

export default Vue.extend({
  name: 'App',
  setup() {
    const { x, y } = useMouse()
    return { x, y }
  }
})
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
