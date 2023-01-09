<template>
  <div class="container w-[100vw] h-[100vh] flex justify-center items-center">
    <div class="w-3/4 h-3/4 shadow-2xl border-2 border-rose-500 rounded-3xl">

      <!-- <TheHeroSection title="Dictionary"/> -->

      <!-- Dictionary -->

      <div class="dictionary w-full h-full pt-5 flex flex-col gap-5 items-start">
        <TheWord v-for="item in wordBase" :key="item" :word="item.spelling" :translate="item.translate" />
      </div>

    </div>


  </div>
</template>

<script>
import TheWord from './components/TheWord.vue';
import TheHeroSection from './components/TheHeroSection.vue';
export default {
  components: {
    TheWord,
    TheHeroSection,
  },

  data() {
    return {
      wordBase: [
        {
          spelling: 'hello',
          translate: 'привет',
          id: '0'
        },
        {
          spelling: 'a case in point',
          translate: 'хороший тому пример',
          id: '1'
        },
      ]
    }
  },
}
</script>

<style>

</style>