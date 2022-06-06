<template>
  <div class="flex flex-col gap-4 mx-auto rounded max-w-fit bg-slate-200 p-4">
    <calculator-display />
    <calculator-controls />
  </div>
</template>

<script>
import CalculatorControls from "./CalculatorControls.vue";
import CalculatorDisplay from "./CalculatorDisplay.vue";
export default {
  components: { CalculatorDisplay, CalculatorControls },
};
</script>

<style></style>
