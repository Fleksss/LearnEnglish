<template>
  <div class="container w-[100vw] h-[100vh] flex justify-center items-center">
    <div class="w-3/4 h-3/4 shadow-2xl border-2 border-rose-500 rounded-3xl relative">

      <!-- TheHeroSection -->
      <transition name="entry">
        <TheHeroSection title="Dictionary" @introduction="introduction" v-if="isClicked" />
      </transition>
      <!--  -->

      <!-- TheWord -->
      <div class="dictionary w-full h-full p-5 flex flex-col gap-5 items-start overflow-y-scroll snap-y"
        v-if="!isClicked">
        <TheWord v-for="item in wordBase" :key="item.id" :word="item.spelling" :translate="item.translate"
          @click="popupClicked = true, popupContent = item" />
      </div>
      <ThePopup v-if="popupClicked" @close="popupClicked = false" :word="popupContent.spelling"
        :translate="popupContent.translate" />
      <!--  -->

      <!-- STATUS: BUGFIX -->
      <!-- <TheWordGame text="fdsafsda" @input="wg, input" /> -->

    </div>


  </div>
</template>

<script>
import TheWord from './components/TheWord.vue';
import TheHeroSection from './components/TheHeroSection.vue';
import ThePopup from './components/ThePopup.vue';
// import TheWordGame from './components/TheWordGame.vue';
export default {
  components: {
    TheWord,
    TheHeroSection,
    ThePopup,
    // TheWordGame,
  },

  data() {
    return {
      isClicked: true,
      popupClicked: false,
      popupContent: '',
      wordBase: [
        {
          spelling: 'a case in point',
          translate: 'хороший тому пример',
          id: 0,
        },
        {
          spelling: 'according to',
          translate: 'согласно c',
          id: 1,
        },
        {
          spelling: 'accurate',
          translate: 'точный',
          id: 2,
        },
        {
          spelling: 'acquire',
          translate: 'приобретать',
          id: 3,
        },
        {
          spelling: 'ancient',
          translate: 'древний',
          id: 4,
        },
        {
          spelling: 'area',
          translate: 'область',
          id: 5,
        },
        {
          spelling: 'arithmetic',
          translate: 'арифметика',
          id: 6,
        },
        {
          spelling: 'around',
          translate: 'вокруг',
          id: 7,
        },
        {
          spelling: 'unambiguous',
          translate: 'однозначный',
          id: 8,
        },
        {
          spelling: 'trade-off',
          translate: 'компромисс',
          id: 9,
        },
        {
          spelling: 'apply',
          translate: 'применять',
          id: 10,
        },
        {
          spelling: 'hello',
          translate: 'привет',
          id: 11,
        },
      ],
    }
  },

  methods: {
    introduction() {
      this.isClicked = false
    },

    // wg() {
    //   if (input === 'word') {
    //     this.answer = true
    //   }
    // }
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