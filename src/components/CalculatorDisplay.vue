<template>
  <div
    class="bg-slate-500 w-full rounded flex flex-col items-end justify-evenly text-white p-2 h-20"
  >
    <div class="flex gap-2">
      <span>{{ secondaryDisplay }}</span>
      <i
        class="fa-solid text-xs flex justify-center items-center"
        :class="`fa-${operation}`"
      ></i>
    </div>
    <div class="text-2xl font-medium">{{ primaryDisplay }}</div>
  </div>
</template>

<script>
export default {
  props: {
    primaryDisplay: String,
    secondaryDisplay: String,
    operation: String,
  },
};
</script>

<style></style>
