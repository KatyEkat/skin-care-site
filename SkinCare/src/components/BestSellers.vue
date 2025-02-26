<script setup>
import { ref, computed } from 'vue'
import LeftArrow from './icons/LeftArrow.vue'
import RightArrow from './icons/RightArrow.vue'

const currentIndex = ref(0)
const totalSlides = 4

const nextSlide = () => {
  if (currentIndex.value < totalSlides - 1) {
    currentIndex.value++
  }
}

const prevSlide = () => {
  if (currentIndex.value > 0) {
    currentIndex.value--
  }
}

const sliderStyle = computed(() => ({
  transform: `translateX(-${currentIndex.value * 100}%)`,
}))
</script>

<template>
  <!-- <div class="best-sellers-block">
    <h2 class="heading">Best sellers</h2>

    <div>
      <div class="slider-arrows">
        <LeftArrow class="arrow" />
        <RightArrow class="arrow" />
      </div>

      <div class="slider-content">
        <div class="card"></div>

        <div class="card"></div>

        <div class="card"></div>

        <div class="card"></div>
      </div>
    </div>
  </div> -->

  <div class="best-sellers-block">
    <h2 class="heading">Best sellers</h2>

    <div>
      <div class="slider-arrows">
        <LeftArrow class="arrow" @click="prevSlide" />
        <RightArrow class="arrow" @click="nextSlide" />
      </div>

      <div class="slider-wrapper">
        <div class="slider-content" :style="sliderStyle">
          <div class="card" v-for="n in totalSlides" :key="n">
            <p class="card-header">Happy jellies</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* .best-sellers-block {
  display: flex;
  margin: 0 46px;
  display: flex;
  flex-direction: column;
  gap: 18px;
}

.heading {
  color: rgb(22, 22, 22);
  font-family: 'Inter Tight';
  font-size: 40px;
  font-weight: 300;
  line-height: 120%;
  letter-spacing: 0.25%;
  text-align: left;
}

.slider-arrows {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  align-items: center;
  gap: 22px;
  padding: 0px;
}

.arrow {
  cursor: pointer;
} */

.best-sellers-block {
  display: flex;
  margin: 0 46px;
  flex-direction: column;
  gap: 18px;
  overflow: hidden;
}

.heading {
  color: rgb(22, 22, 22);
  font-family: 'Inter Tight';
  font-size: 40px;
  font-weight: 300;
  line-height: 120%;
  text-align: left;
}

.slider-arrows {
  display: flex;
  justify-content: flex-end;
  gap: 22px;
}

.arrow {
  cursor: pointer;
}

.slider-wrapper {
  overflow: hidden;
  width: 100%;
}

.slider-content {
  display: flex;
  transition: transform 0.3s ease-in-out;
  width: 400%;
}

.card {
  width: 313px;
  height: 426px;

  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  gap: 20px;
}

.card-header {
  color: rgb(22, 22, 22);
  font-family: 'Inter Tight';
  font-size: 24px;
  font-weight: 300;
  line-height: 140%;
  letter-spacing: 0.15%;
  text-align: left;

  box-sizing: border-box;
  border-bottom: 1px solid rgb(224, 217, 226);
}
</style>
