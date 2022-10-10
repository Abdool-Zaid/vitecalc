<script setup>
let i;
let percentage;
let score = [];
let fonts = [
  "Alkalami",
  "Anton",
  "Bitter",
  "Comforter Brush",
  "DM Sans",
  "Gemunu Libre",
  "Inconsolata",
  "Indie Flower",
  "Lato",
  "Lobster",
  "Merriweather Sans",
  "Noto Sans",
  "Noto Sans Ethiopic",
  "Noto Serif Display",
  "Nunito Sans",
  "Peralta",
  "PT Serif",
  "Silkscreen",
  "cursive",
  "Titillium Web",
  "sans-serif",
  "serif",
];
function generateRandomColor() {
  console.log("clicked");
  let letters = "0123456789ABCDEF";
  let color = "#";
  for (i = 0; i < 8; i++) {
    color += letters[Math.floor(Math.random() * 16)];
  }
  return color;
}
function generateRandomPercentage() {
  percentage = Math.random() * 100 + "%";
  return percentage;
}
console.log(generateRandomPercentage());
</script>

<template>
  <div>
  <div id="score" class="">
<p>score</p>

  </div>
  </div>
  <p></p>
</template>
<style>
  *{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    word-wrap: break-word;
  }
  ::-webkit-scrollbar {
    display:none
  }
  .material-symbols-outlined {
    font-variation-settings:
    'FILL' 0,
    'wght' 400,
    'GRAD' 0,
    'opsz' 48
  }
  </style>