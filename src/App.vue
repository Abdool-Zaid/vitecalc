<script setup>
  let i
  let percentage 
function generateRandomColor() {
  console.log('clicked')
  let letters = "0123456789ABCDEF";
  let color = "#";
  for ( i = 0; i < 8; i++) {
    color += letters[Math.floor(Math.random() * 16)];
  }
  return color;
}
function generateRandomPercentage(){
percentage=(Math.random()*100)+'%'
return percentage
}
console.log(
generateRandomPercentage()
)

</script>

<template>
<button v-on:click="generateRandomColor()">click</button>
<p></p>
</template>
<style>

</style>
