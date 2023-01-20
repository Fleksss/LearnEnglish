<template>
  <div class="layer fixed left-0 top-0 w-full h-full flex justify-center items-center" @click="$emit('close')">
    <div class="modal p-5 rounded-md bg-white w-[400px]" @click.stop>
      <div class="content">
        <p class="text-center mb-5 text-2xl">
          {{ word }}
        </p>
        <p class="text-center mb-5 text-2xl">
          {{ translate }}
        </p>
      </div>
      <button class="text-white uppercase py-2 px-5 rounded-md bg-gray-700 mt-3 block mx-auto" @click="$emit('close')">
        Close
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    word: String,
    translate: String
  }
}
</script>

<style>
.layer {
  background: rgba(0, 0, 0, 0.9);
}
</style>