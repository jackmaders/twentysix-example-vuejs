<template>
  <calculator-history />
  <calculator-display />
  <calculator-controls />
</template>

<script>
import CalculatorControls from "./CalculatorControls.vue";
import CalculatorDisplay from "./CalculatorDisplay.vue";
import CalculatorHistory from "./CalculatorHistory.vue";
export default {
  components: { CalculatorDisplay, CalculatorControls, CalculatorHistory },
};
</script>

<style></style>
