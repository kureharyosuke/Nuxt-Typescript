<template>
  <div class="main">
    <h1>{{ Hello }}</h1>
    <h1>{{ Vue }}</h1>
    <h1>{{ TypeScript }}</h1>
    <h1>{{ Nuxt }}</h1>
    <h1>{{ fullMessage }}</h1>
    <h3>{{ counter }}</h3>
    <button @click="incrementcounter()">Button</button>
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator'

@Component
export default class HelloVue extends Vue {
  @Prop() private msg!: string
  Hello = 'Hello 😳 '
  Vue = 'Vue 😥 '
  TypeScript = 'TypeScript 😰 '
  Nuxt = 'Nuxt 😱 '
  counter = 0

  get fullMessage(): String {
    return this.Hello + this.Vue + this.TypeScript + this.Nuxt
  }

  incrementcounter() {
    this.counter++
  }
}
</script>
<style scoped>
.main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vw;
}
</style>
>
