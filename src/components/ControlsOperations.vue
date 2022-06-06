<template>
  <div class="grid grid-cols-1 gap-4">
    <button
      v-for="symbol in ['+', '-', 'x', '÷']"
      :key="symbol"
      class="col-span-2 flex justify-center items-center w-16 h-16 rounded transition-all bg-blue-300 hover:bg-blue-400 hover:scale-105"
    >
      +
    </button>
  </div>
</template>

<script>
export default {};
</script>

<style></style>
