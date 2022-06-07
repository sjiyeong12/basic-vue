<template>
  <div id="app">
    <p>{{title}}</p>
    <counter></counter>
    <counter></counter>
    <counter></counter>
  </div>
</template>

<script>
import { createApp } from '@vue/runtime-dom'
  const app = createApp({})
  app.component('counter',{
    inject:['counter_header'],
    setup(){
    const count = ref(0)
    return{count}
  },
  template:` <span>{{counter_head}}</span>
  <button @click ="count++" v-text="count" />
  <hr>`,
  })
  app.config.globalProperties.title = 'Vue 3 Demo'
  app.provide('counter_header', 'Counter')
  app.mount('#app')
export default {
}
</script>

<style>

</style>