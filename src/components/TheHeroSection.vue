<template>
  <div class="w-full h-full flex justify-center items-center cursor-pointer absolute top-0 left-0x z-10"
    @click="$emit('introduction')">
    <h1 class="text-7xl text-gray-500">
      {{ title }}
    </h1>
  </div>
</template>

<script>
export default {
  props: {
    title: String
  }
}
</script>

<style>

</style>