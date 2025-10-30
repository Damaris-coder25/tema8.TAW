<script setup>
import{ref} from 'vue'

const culoare = ref('rgb(255,0,0)')

function genereazaCuloare() {
  const r = Math.floor(Math.random() * 256)
  const g = Math.floor(Math.random() * 256)
  const b = Math.floor(Math.random() * 256)
  culoare.value = `rgb(${r}, ${g}, ${b})`
  console.log('Culoare nouă:', culoare.value)
}

</script>

<template>
<button 
  @click="genereazaCuloare"
  style="margin-left:70px; 
  margin-top:30px"
  >Genereaza culoare
</button>
<br>
<div
  :style="{
    width: '90px',
    height: '90px', 
    backgroundColor: culoare,
    marginLeft: '90px',
    marginTop: '30px'
  }">
</div>
</template>

<style scoped>
</style>
