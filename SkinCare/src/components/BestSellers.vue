<script setup>
import { ref, computed } from 'vue'
import LeftArrow from './icons/LeftArrow.vue'
import RightArrow from './icons/RightArrow.vue'
import { products, iconsMap } from '../API/ApiVue'

const currentIndex = ref(0)

const cardWidth = 313
const cardGap = 32
const step = cardWidth + cardGap

const totalSlides = computed(() => products.length)

const nextSlide = () => {
  currentIndex.value = (currentIndex.value + 1) % totalSlides.value
}

const prevSlide = () => {
  currentIndex.value = (currentIndex.value - 1 + totalSlides.value) % totalSlides.value
}

const sliderStyle = computed(() => ({
  transform: `translateX(-${currentIndex.value * step}px)`,
  transition: 'transform 0.3s ease-in-out',
}))
</script>

<template>
  <div class="best-sellers-block">
    <h2 class="heading">Best sellers</h2>

    <div>
      <div class="slider-arrows">
        <LeftArrow class="arrow" @click="prevSlide" />
        <RightArrow class="arrow" @click="nextSlide" />
      </div>

      <div class="slider-wrapper">
        <div class="slider-content" :style="sliderStyle">
          <div class="card" v-for="product in products" :key="product.id">
            <component :is="iconsMap[product.icon]" />
            <div class="card-text-content">
              <p class="card-header">{{ product.name }}</p>
              <p class="card-price">{{ product.price }}</p>
            </div>
            <p class="card-description">{{ product.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
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
  width: 00%;
  gap: 32px;
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

.card-text-content {
  box-sizing: border-box;
  border-bottom: 1px solid rgb(224, 217, 226);

  padding-bottom: 8px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.card-header {
  color: rgb(22, 22, 22);
  font-family: 'Inter Tight';
  font-size: 24px;
  font-weight: 300;
  line-height: 140%;
  text-align: left;
}

.card-price {
  color: rgb(91, 91, 91);
  font-family: 'Inter Tight';
  font-size: 20px;
  font-weight: 400;
  line-height: 140%;
  text-align: left;
}

.card-description {
  color: rgb(22, 22, 22);
  font-family: 'Inter';
  font-size: 16px;
  font-weight: 400;
  line-height: 150%;
  text-align: left;
}
</style>
