<template>
  <div class="grid grid-cols-3 gap-4">
    <button
      class="flex justify-center items-center w-16 h-16 rounded transition-all bg-slate-400 hover:bg-slate-500 hover:scale-105"
      v-for="index in 9"
      :key="index"
    >
      {{ index }}
    </button>
    <button
      class="flex justify-center items-center w-16 h-16 rounded bg-slate-400 transition-all hover:bg-slate-500 hover:scale-105"
    >
      0
    </button>

    <button
      class="col-span-2 flex justify-center items-center w-36 h-16 rounded bg-orange-300 transition-all hover:bg-orange-400 hover:scale-105"
    >
      =
    </button>
  </div>
</template>

<script>
export default {
  components: {},
};
</script>

<style></style>
