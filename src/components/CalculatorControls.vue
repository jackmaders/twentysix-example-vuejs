<template>
  <div class="grid grid-cols-4 gap-4">
    <calculator-button buttonType="control" @click="$emit('clearDisplay')"
      ><i class="fa-solid fa-ban"></i>
    </calculator-button>
    <calculator-button buttonType="control" @click="$emit('deleteCharacter')"
      ><i class="fa-solid fa-delete-left"></i>
    </calculator-button>
    <calculator-button buttonType="number" @click="$emit('appendCharacter', 1)">
      <i class="fa-solid fa-1"></i>
    </calculator-button>
    <calculator-button buttonType="number" @click="$emit('appendCharacter', 2)">
      <i class="fa-solid fa-2"></i>
    </calculator-button>
    <calculator-button buttonType="number" @click="$emit('appendCharacter', 3)">
      <i class="fa-solid fa-3"></i>
    </calculator-button>
    <calculator-button
      buttonType="operation"
      @click="$emit('setOperation', 'plus')"
    >
      <i class="fa-solid fa-plus"></i>
    </calculator-button>
    <calculator-button buttonType="number" @click="$emit('appendCharacter', 4)">
      <i class="fa-solid fa-4"></i>
    </calculator-button>
    <calculator-button buttonType="number" @click="$emit('appendCharacter', 5)">
      <i class="fa-solid fa-5"></i>
    </calculator-button>
    <calculator-button buttonType="number" @click="$emit('appendCharacter', 6)">
      <i class="fa-solid fa-6"></i>
    </calculator-button>
    <calculator-button
      buttonType="operation"
      @click="$emit('setOperation', 'minus')"
    >
      <i class="fa-solid fa-minus"></i>
    </calculator-button>
    <calculator-button buttonType="number" @click="$emit('appendCharacter', 7)">
      <i class="fa-solid fa-7"></i>
    </calculator-button>
    <calculator-button buttonType="number" @click="$emit('appendCharacter', 8)">
      <i class="fa-solid fa-8"></i>
    </calculator-button>
    <calculator-button buttonType="number" @click="$emit('appendCharacter', 9)">
      <i class="fa-solid fa-9"></i>
    </calculator-button>
    <calculator-button
      buttonType="operation"
      @click="$emit('setOperation', 'times')"
    >
      <i class="fa-solid fa-times"></i>
    </calculator-button>
    <calculator-button buttonType="number" @click="$emit('appendCharacter', 0)">
      <i class="fa-solid fa-0"></i>
    </calculator-button>
    <calculator-button
      buttonType="number"
      @click="$emit('appendCharacter', '.')"
    >
      <i class="fa-solid fa-circle"></i>
    </calculator-button>
    <calculator-button buttonType="calculate" @click="$emit('calculateAnswer')">
      <i class="fa-solid fa-equals"></i>
    </calculator-button>
    <calculator-button
      buttonType="operation"
      @click="$emit('setOperation', 'divide')"
    >
      <i class="fa-solid fa-divide"></i>
    </calculator-button>
  </div>
</template>

<script>
import CalculatorButton from "./CalculatorButton.vue";

export default {
  components: { CalculatorButton },
  emits: [
    "clearDisplay",
    "appendCharacter",
    "deleteCharacter",
    "setOperation",
    "calculateAnswer",
  ],
};
</script>

<style></style>
