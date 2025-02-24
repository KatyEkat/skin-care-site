<script setup>
import MainImage from './icons/MainImage.vue'
import CirclreImgLight from './icons/CirclreImgLight.vue'
</script>

<template>
  <div class="background-content">
    <div class="background">
      <div class="text-block">
        <h1 class="main-text">Treart your skin like never before</h1>
        <p class="main-description">
          Experience the difference with our products, designed to reduce redness, irritation, and
          discomfort, leaving your skin feeling healthy.
        </p>

        <div class="miniblock">
          <CirclreImgLight />
          <p class="button">Discover now</p>
          <!-- <button class="button">Discover now</button> -->
        </div>
      </div>
    </div>
    <MainImage class="background-img" />
  </div>
</template>

<style>
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

.text-block {
  display: flex;
  flex-direction: column;
  gap: 20px;
  max-width: 429px;
  justify-content: center;
  height: 100%;
  margin-left: 45px;
}

.main-text {
  color: rgb(255, 255, 255);
  font-family: 'Inter Tight';
  font-size: 58px;
  font-weight: 400;
  line-height: 110%;
  letter-spacing: 0%;
  text-align: left;
}

.main-description {
  color: rgb(255, 255, 255);
  font-family: 'Inter';
  font-size: 16px;
  font-weight: 400;
  line-height: 150%;
  letter-spacing: 0%;
  text-align: left;
}

.button {
  color: rgb(255, 255, 255);
  font-family: 'Inter';
  font-size: 16px;
  font-weight: 400;
  line-height: 140%;
  letter-spacing: 0%;
  text-align: left;
}

.miniblock {
  display: flex;
  gap: 12px;
  align-items: center;
}
</style>
