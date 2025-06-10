<script setup>
import GrayIcon from './icons/GrayIcon.vue'
</script>

<template>
  <div class="shop">
    <div class="shop-block">
      <div class="shop-content">
        <h2 class="shop-header">Shop by area</h2>
        <div class="shop-menu">
          <p class="shop-menu-item">Face</p>
          <p class="shop-menu-item">Body</p>
          <p class="shop-menu-item">Hair & Eyelash</p>
          <p class="shop-menu-item">Nails</p>
        </div>
      </div>

      <div class="shop-img">
        <GrayIcon />
      </div>
    </div>
  </div>
</template>

<style scoped>
.shop {
  border-bottom: 1px solid rgb(224, 217, 226);
}

.shop-block {
  display: grid;
  grid-template-columns: 1fr 1fr;
  margin: 65px 46px 120px 46px;
}

.shop-content {
  display: flex;
  flex-direction: column;
  gap: 48px;
}

.shop-header {
  color: rgb(22, 22, 22);
  font-family: 'Inter';
  font-size: 14px;
  font-weight: 400;
  line-height: 150%;
  letter-spacing: 0.4%;
  text-align: left;
}

.shop-menu {
  display: flex;
  flex-direction: column;
  max-width: 660px;
}

.shop-menu-item {
  color: rgb(114, 114, 114);
  font-family: 'Inter Tight';
  font-size: 68px;
  font-weight: 300;
  line-height: 140%;
  text-align: left;
  border-bottom: 1px solid rgb(224, 217, 226);
  padding-bottom: 10px;
}

.shop-img {
  display: flex;
  justify-content: flex-end;
}
</style>
