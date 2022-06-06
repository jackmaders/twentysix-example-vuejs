<template>
  <div class="flex flex-col gap-4 mx-auto rounded max-w-fit bg-slate-200 p-4">
    <calculator-display
      :primaryDisplay="currentOperand"
      :secondaryDisplay="previousOperand"
      :operation="operation"
    />
    <calculator-controls
      @clearDisplay="clearDisplay()"
      @deleteCharacter="deleteCharacter()"
      @appendCharacter="appendCharacter($event)"
      @setOperation="setOperation($event)"
      @calculateAnswer="calculateAnswer()"
    />
  </div>
</template>

<script>
import CalculatorControls from "./CalculatorControls.vue";
import CalculatorDisplay from "./CalculatorDisplay.vue";
export default {
  components: { CalculatorDisplay, CalculatorControls },
  methods: {
    clearDisplay: function () {
      this.currentOperand = "";
      this.previousOperand = "";
    },
    deleteCharacter: function () {
      this.currentOperand = this.currentOperand.toString().slice(0, -1);
    },
    appendCharacter: function (character) {
      if (this.operation === "" && this.previousOperand !== "") return;
      if (character === "." && this.currentOperand.includes(".")) return;

      this.currentOperand =
        this.currentOperand.toString() + character.toString();
    },
    setOperation: function (operation) {
      if (this.currentOperand === ".") return;

      if (this.previousOperand !== "") {
        this.operation = operation;
      } else {
        this.previousOperand = this.currentOperand;
        this.currentOperand = "";
        this.operation = operation;
      }
    },
    calculateAnswer: function () {
      const previousValue = parseFloat(this.previousOperand);
      const currentValue = parseFloat(this.currentOperand);

      if (this.currentOperand === "" || this.previousOperand === "") return;
      if (isNaN(previousValue) || isNaN(currentValue)) return;

      switch (this.operation) {
        case "plus":
          this.previousOperand = String(previousValue + currentValue);
          break;
        case "minus":
          this.previousOperand = String(previousValue - currentValue);
          break;
        case "times":
          this.previousOperand = String(previousValue * currentValue);
          break;
        case "divide":
          if (currentValue === 0) return;
          this.previousOperand = String(previousValue / currentValue);
          break;
        default:
          return;
      }

      this.currentOperand = "";
      this.operation = "";
    },
  },
  data() {
    return {
      currentOperand: "",
      previousOperand: "",
      operation: "",
    };
  },
};
</script>

<style></style>
