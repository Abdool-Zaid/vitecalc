<script setup>


</script>

<template>
<h1>home</h1>
<div class="container">
  <div class="head"></div>
  <div class="body"></div>
  <div class="tears-left"></div>
  <div class="tears-right"></div>
</div>
</template>
<style scoped >
.container {  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr 1fr;
  gap: 0px 0px;
  grid-auto-flow: row;
  grid-template-areas:
    ". head ."
    "tears-left body tears-right"
    "tears-left . tears-right";
}

.head { grid-area: head; }

.body { grid-area: body; }

.tears-left { grid-area: tears-left; }

.tears-right { grid-area: tears-right; }

</style>
