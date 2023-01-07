<template>
  <p class="text-gray-400 text-4xl">
    {{ word }}
  </p>

  <span class="text-gray-400 text-4xl">
    {{ translate }}
  </span>

</template>

<script>
export default {
  props: {
    word: String,
    translate: String
  }
}
</script>

