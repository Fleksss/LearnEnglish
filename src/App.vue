<template>
  <div class="container w-[100vw] h-[100vh] flex justify-center items-center">
    <div class="w-[500px] h-[400px] shadow-2xl relative border-2 border-rose-500 rounded-3xl">
      <h1 class="text-4xl text-gray-500 absolute top-[40px] left-1/3 right-1/3">Dictionary</h1>
      <div class="w-full h-full pt-[110px] flex justify-evenly items-start">
        <TheWord v-for="item in wordBase" :key="item" :word="item.spelling" :translate="item.translate" />
      </div>
    </div>
  </div>
</template>

<script>
import TheWord from './components/TheWord.vue';
export default {
  components: {
    TheWord
  },

  data() {
    return {
      wordBase: [
        {
          spelling: 'hello',
          translate: 'привет',
        }
      ]
    }
  }
}
</script>

<style>

</style>