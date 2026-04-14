<template>
  <div>
    <v-card>
      <v-card-text>
        <v-icon size="50" inline>mdi-calculator</v-icon>
        <h1>Calculator</h1>

        <v-radio-group v-model="operator" inline="">
           <v-radio label="Addition" value="add"></v-radio>
           <v-radio label="Subtraction" value="subtract"></v-radio>
           <v-radio label="Multiplication" value="multiply"></v-radio>
           <v-radio label="Division" value="divide"></v-radio>
        </v-radio-group>
   
        <h2>Selected Operator: {{ operator }}</h2>
        <v-text-field label = "Enter first number" v-model="firstnumber"></v-text-field>
        <v-text-field label = "Enter second number" v-model="secondnumber" ></v-text-field>
        <v-text-field label = "Result" readonly v-model="result"></v-text-field>

        <v-btn @click="calculate" color="blue">Calculate</v-btn>
      </v-card-text>
    </v-card>
  </div>
</template>

<script  setup>
const operator = ref(null);
const firstnumber = ref();
const secondnumber = ref();
const result = ref();

function calculate() {
  if( operator.value ==="add") {
    result.value = Number(firstnumber.value) + Number(secondnumber.value);
  } else if (operator.value==="subtract") {
    result.value = Number(firstnumber.value) - Number(secondnumber.value);
  } else if (operator.value==="multiply") {
    result.value = Number(firstnumber.value) * Number(secondnumber.value);
  } else if (operator.value==="divide") {
    result.value = Number(firstnumber.value) / Number(secondnumber.value);
  }
}

</script>

<style>

</style>