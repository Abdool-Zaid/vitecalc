<script setup></script>

<template>
  <div class="container">
    <div class="head">head</div>
    <div class="body">body</div>
    <div class="tears-left"></div>
    <div class="tears-right"></div>
  </div>
</template>
<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  word-wrap: break-word;
}
::-webkit-scrollbar {
  display: none;
}
:root {
  --glass: #ae36b225;
  --sixty: #88888800;
  --bg: #2a51be;
  --thirty: #006c8d;
  --acc: #4e0000;
  --ss: 1%;
  --se: 1em;
  --snx: 30vw;
  --height: 80vh;
  --width: 70vw;
  --sny: 40vh;
  --bubblebg: #cfcbcb;
  --mute: #00000000;
  --cursor: #e600ff;
}
html {
  width: 100vw;
  height: 100vh;
  position: fixed;
  left: 0;
  top: 0;
}
/* body {
  overflow-y: hidden;
  background-image: radial-gradient(
    circle,
    #664cc5,
    #ad36b2,
    #dc1491,
    #f71069,
    #ff3e3e
  );
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-position: center;
  background-size: 100vw 100vh;
} */
.head {
  background-color: burlywood;
  /* height: 20vh; */
  border-radius: 50%;
  bottom: 0;
}
.body {
  background-color: burlywood;
  aspect-ratio: 1;
  border-radius: 50%;
}
.tears-left {
  background-color: blue;
  height: 90vh;
  width: 10vw;
  z-index: 20;
}
.tears-right {
  background-color: blue;
  height: 90vh;
  width: 10vw;
  z-index: 20;
}
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr 1fr 1fr 1fr;
  gap: 0px 0px;
  grid-auto-flow: row;
}

.body {
  grid-area: 3 / 2 / 6 / 6;
}

.head {
  grid-area: 1 / 3 / 3 / 5;
}

.tears-left {
  grid-area: 1 / 1 / 6 / 3;
}

.tears-right {
  grid-area: 1 / 5 / 6 / 7;
}

.tears-left {
  grid-area: tears-left;
}

.tears-right {
  grid-area: tears-right;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: var(--acc);
}
@media (min-width: 1024px) {
}
</style>
