<template>
  <img
    class="VuetifyLogo"
    alt="Vuetify Logo"
    src="/t.png"
  >
</template>

<style>
.VuetifyLogo {
  height:400px;
  width: 400px;
  transform: rotateY(560deg);
  animation: turn 3.5s ease-out forwards 1s;
}

@keyframes turn {
  100% {
    transform: rotateY(0deg);
  }
}
</style>
