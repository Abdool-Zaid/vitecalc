<script setup>
let i;
let occational = "!";
let percentage;
let score = JSON.parse(localStorage.getItem("score"))
  ? JSON.parse(localStorage.getItem("score"))
  : localStorage.setItem("score", JSON.stringify(0));
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
  let letters = "0123456789ABCDEF";
  let color = "#";
  for (i = 0; i < 6; i++) {
    color += letters[Math.floor(Math.random() * 16)];
  }
  return color;
}
function generateRandomPercentage() {
  percentage = Math.random() * 100 + "%";
  return percentage;
}
function getFont() {
  i = Math.round(fonts.length * Math.random());
  return fonts[i];
}
function generateBorderSize() {
  i = Math.round(10 * Math.random()) + "px";
  return i;
}
function itterateScore(id) {
  i = -1;
  document.querySelectorAll("button").forEach((button) => {
    i++;
    button.classList = "";
  });
  let length = i;
  if (document.querySelector("#" + id).classList.contains('active')) {
    alert("betterluck next time");
    localStorage.setItem("score", JSON.stringify(0));
    document.querySelector("p").innerHTML = `score ${score}`;
    document.querySelectorAll("button").forEach((button) => {
      button.style.backgroundColor = "";
      button.style.color = "";
      button.style.borderRadius = "";
      button.style.borderWidth = "";
      button.style.borderColor = "";
      button.style.fontFamily = "";
    });
  } else {
    score++;
    document.querySelector("p").innerHTML = `score ${score}`;
    localStorage.setItem("score", JSON.stringify(score));
    document.querySelectorAll("button").forEach((button) => {
      button.style.backgroundColor = generateRandomColor();
      button.style.color = generateRandomColor();
      button.style.borderRadius = generateRandomPercentage();
      button.style.borderWidth = generateBorderSize();
      button.style.borderColor = generateRandomColor();
      button.style.fontFamily = getFont();
    });
  }
  document.querySelectorAll("button")[Math.round(length * Math.random())].classList.toggle("active");
}
</script>

<template>
  <div class="w-4/5 flex flex-col items-center">
    <div id="score" class="flex flex-row items-center">
      <p>score</p>
      <img src="./assets/logoFinal.ico" alt="endless mode" />
    </div>
    <div class="flex flex-col">
      <button id="option0" v-on:click="itterateScore('option0')" class="active">
        Download
      </button>
      <button id="option1" v-on:click="itterateScore('option1')">
        Download
      </button>
    </div>
  </div>
  <p></p>
</template>
<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
::-webkit-scrollbar {
  display: none;
}
.material-symbols-outlined {
  font-variation-settings: "FILL" 0, "wght" 400, "GRAD" 0, "opsz" 48;
}
img {
  height: 16px;
  width: 16px;
}
button {
  margin: 1%;
  padding: 1em;
}
</style>
