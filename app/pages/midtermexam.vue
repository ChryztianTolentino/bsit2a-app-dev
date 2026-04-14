<template>
  <div>
    <v-row>
      <v-col>
        <v-card>
          <v-card-text>
             <v-icon size="60"> mdi-calculator</v-icon>
            <v-radio-group v-model="operator" inline>

              <!-- Operator Selection -->
               
                <v-radio  label="Addition" value="one"></v-radio>
                <v-radio  label="Subtraction" value="two"></v-radio>
                <v-radio  label="Multiplication" value="three"></v-radio>
                <v-radio  label="Division" value="four"></v-radio>

          </v-radio-group>

            <h2>Selected Operator:</h2>

                <v-text-field v-model="num1" label="Enter 1st Number"></v-text-field>
                <v-text-field v-model="num2" label="Enter 2nd Number"></v-text-field>
                <v-text-field v-model="total" label="Total : "></v-text-field>
                <v-btn color="primary" @click="midtermexam" block>calculate</v-btn>

          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script setup>

const num1 = ref();  
const num2 = ref();
const total = ref();
const operator = ref();

function midtermexam() {
if (operator.value === 'one') {
    total.value = Number(num1.value) + Number(num2.value);
} else if (operator.value === 'two') {
    total.value = Number(num1.value) - Number(num2.value);
} else if (operator.value === 'three') {
    total.value = Number(num1.value) * Number(num2.value);
} else if (operator.value === 'four') {
    total.value = Number(num1.value) / Number(num2.value);    
}
}
</script>

<style>

</style>