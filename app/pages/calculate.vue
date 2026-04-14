<template>
<<<<<<< HEAD
    <div>
        <h1> Calculate page</h1>
    </div>

    <v-card width="500">
        <v-card-text>
            <v-form>
                <v-text-field v-model="firstnumber" label="Enter 1st Number"></v-text-field>
                <v-text-field v-model="secondnumber" label="Enter 2nd Number"></v-text-field>
                <v-text-field v-model="total" label="Total : "></v-text-field>
                <v-btn color="primary" @click="calculate" block>calculate</v-btn>
            </v-form>
        </v-card-text>
    </v-card>


</template>

<script setup>
const firstnumber = ref();
const secondnumber = ref();
const total = ref(0);

function calculate () {
    total.value = Number(firstnumber.value) + Number(secondnumber.value);`1w`
}
</script>
=======
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
>>>>>>> b609793473987f2acb68f98c6fb52fc152b6eddf
