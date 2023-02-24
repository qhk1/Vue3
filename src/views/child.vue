<script setup>
import {ref, inject} from 'vue'
const name = inject('name')
const number = inject('number')
function add() {
    number ++
}
</script>

<template>
  <div>
    <p @click="add">{{number}}</p>
  </div>
  
</template>