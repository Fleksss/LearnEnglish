<template>
  <div class="">
    <h1>
      {{ text }}
    </h1>
    <input type="text" :v-model="input" @focus="$emit('input')">
    <h1>{{ answer }}</h1>
  </div>
</template>

<script>
export default {
  props: {
    text: String,
    input: {
      type: String,
      default: input
    }
  },
  data() {
    return {
      answer: false
    }
  },
}
</script>

<style>

</style>