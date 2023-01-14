<template>
  <div class="flex justify-center items-start w-full border-2 border-green-500 rounded-3xl shadow-2xl p-5 snap-center">
    <div class="w-1/2">
      <p class="text-gray-400 text-3xl px-5 text-left">
        {{ word }}
      </p>
    </div>

    <div class="w-1/2">
      <p class="text-gray-400 text-3xl px-5 text-left">
        {{ translate }}
      </p>
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
