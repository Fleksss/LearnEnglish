<template>
  <div class="flex justify-evenly items-start w-full">
    <p class="text-gray-400 text-3xl inline-block">
      {{ word }}
    </p>

    <p class="text-gray-400 text-3xl inline-block">
      {{ translate }}
    </p>
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

