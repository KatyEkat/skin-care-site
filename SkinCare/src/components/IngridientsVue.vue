<script setup>
import Mint from './icons/MintIcon.vue'
import Salt from './icons/SaltIcon.vue'
import DarkDot from './icons/DarkDot.vue'
</script>

<template>
  <div>
    <div>
      <h2 class="header">Our ingredients</h2>
      <div>
        <h3>We are inspired by nature</h3>
        <p>
          Our vegan and cruelty-free formulas harness the power of natural, safe ingredients to
          gently soothe, balance, and strengthen your skin's natural barrier. All ingredients we use
          derived from mother nature ans are absolutely harmless both for you, and for the
          environment.
        </p>
        <div>
          <DarkDot />
          <p>Discover Now</p>
        </div>
      </div>
    </div>

    <div>
      <Mint />
      <Salt />
    </div>
  </div>
</template>

<style scoped>
.header {
  color: rgb(22, 22, 22);
  font-family: 'Inter';
  font-size: 14px;
  font-weight: 400;
  line-height: 150%;
  text-align: left;
}
</style>
