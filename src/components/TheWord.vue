<template>
  <div
    class="flex justify-center items-start w-full border-2 border-green-500 rounded-3xl shadow-2xl p-5 snap-center text-gray-400  hover:text-blue-400 cursor-pointer">
    <div class="w-1/2">
      <p class="text-3xl px-5 text-left">
        {{ word }}
      </p>
    </div>

    <div class="w-1/2">
      <p class="text-3xl px-5 text-left">
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
