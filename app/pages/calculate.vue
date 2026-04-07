<template>
  <div>
    <h1>Calculate Page</h1>
    <v-card width="500">
      <v-card-text>
        <v-form>
          <v-text-field v-model="firstnumber" label="Enter 1st Number"></v-text-field>
          <v-text-field v-model="secondnumber" label="Enter 2nd Number"></v-text-field>
          <v-text-field v-model="total" label="Total: "></v-text-field>
          </v-form>
        <v-btn color="red" @click="calculate"> Calculate </v-btn>
        </v-card-text>
      </v-card>
    </div>
  </template>

<script setup>

const firstnumber = ref()
const secondnumber = ref()
const total = ref()

// function to calculate the total
function calculate () {
    total.value = Number(firstnumber.value) + Number(secondnumber.value)
}
</script>

<style>

</style> 