<template>
  <div class="container w-[100vw] h-[100vh] flex justify-center items-center">
    <div class="w-3/4 h-3/4 shadow-2xl border-2 border-rose-500 rounded-3xl relative">
      <!-- <transition name="entry">
        <TheHeroSection title="Dictionary" @introduction="introduction" v-if="isClicked" />
      </transition>

      <div class="dictionary w-full h-full p-5 flex flex-col gap-5 items-start overflow-y-scroll snap-y"
        v-if="!isClicked">
        <TheWord v-for="item in wordBase" :key="item" :word="item.spelling" :translate="item.translate" />
      </div> -->
      <TheWordGame :text="'fdsafsda'" />
    </div>


  </div>
</template>

<script>
import TheWord from './components/TheWord.vue';
import TheHeroSection from './components/TheHeroSection.vue';
import TheWordGame from './components/TheWordGame.vue';
export default {
  components: {
    TheWord,
    TheHeroSection,
    TheWordGame,
  },

  data() {
    return {
      isClicked: true,
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
        {
          spelling: 'according to',
          translate: 'согласно c',
          id: '2'
        },
        {
          spelling: 'accurate',
          translate: 'точный',
          id: '3'
        },
        {
          spelling: 'acquire',
          translate: 'приобретать',
          id: '4'
        },
        {
          spelling: 'ancient',
          translate: 'древний',
          id: '5'
        },
        {
          spelling: 'area',
          translate: 'область',
          id: '6'
        },
        {
          spelling: 'arithmetic',
          translate: 'арифметика',
          id: '7'
        },
        {
          spelling: 'around',
          translate: 'вокруг',
          id: '8'
        },
        {
          spelling: 'unambiguous',
          translate: 'однозначный',
          id: '9'
        },
        {
          spelling: 'trade-off',
          translate: 'компромисс',
          id: '10'
        },
        {
          spelling: 'apply',
          translate: 'применять',
          id: '11'
        },
      ],
    }
  },
  methods: {
    introduction() {
      this.isClicked = false
    }
  }
}
</script>

<style>
.entry-enter-active,
.entry-leave-active {
  transition: all 1s;
}

.entry-enter-from,
.entry-leave-to {
  opacity: 0;
}
</style>