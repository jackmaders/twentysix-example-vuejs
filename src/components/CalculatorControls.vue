<template>
  <div class="flex gap-4">
    <controls-numbers />
    <controls-operations />
  </div>
</template>

<script>
import ControlsNumbers from "./ControlsNumbers.vue";
import ControlsOperations from "./ControlsOperations.vue";
export default {
  components: { ControlsOperations, ControlsNumbers },
};
</script>

<style></style>
