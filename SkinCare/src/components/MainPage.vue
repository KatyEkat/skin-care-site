<script setup>
import MainImage from './icons/MainImage.vue'
</script>

<template>
  <div class="background-content">
    <div class="background"></div>
    <MainImage class="background-img" />
  </div>
</template>

<style>
/* .background-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  top: 0;
  position: absolute;
  z-index: -1;
}

.background {
  background: rgb(153, 46, 73);
}

.background-img {
} */

.background-content {
  display: grid;
  grid-template-columns: 1fr 1fr; 
  width: 100vw;
  /* height: 830px; */
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
}

.background {
  background: rgb(153, 46, 73);
  width: 100%;
  height: 100%;
}

.background-img {
  width: 100%;
  height: 100%;
  display: flex; 
  align-items: center;
  justify-content: center;
}

.background-img svg {
  width: 100%;
  height: 100%;
  object-fit: cover; 
}


</style>
