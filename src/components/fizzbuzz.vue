<script setup lang="ts">
import {ref} from 'vue'

let input: number

const result = ref( function(input) {
  const isFizz = input.value % 3 == 0,
        isBuzz = input.value % 5 == 0
  return isFizz ?
    ( isBuzz ? "FizzBuzz" : "Fizz" ) :
    ( isBuzz ? "Buzz" : input.value )
})

</script>

<template>
  <div class="fizzbuzz">
    <input v-model="input">
    <p>{{ result }}</p>
  </div>
</template>

<style>

</style>