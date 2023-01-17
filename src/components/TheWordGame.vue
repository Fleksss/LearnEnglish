<template>
  <div class="">
    <input type="text" v-model="input" @click.shift="wg">
    <h1>
      {{ text }}
    </h1>
    <h1>{{ answer }}</h1>
  </div>
</template>

<script>
export default {
  props: {
    text: String,
  },
  data() {
    return {
      answer: false
    }
  },
  methods: {
    wg() {
      if (input === 'word') {
        this.answer = true
        console.log('fdsa');

      }
    }
  }
}
</script>

<style>

</style>