<script setup>
import CirclreImgDark from './icons/CirclreImgDark.vue'
import AllInOneYellow from './icons/AllInOneYellow.vue'
import BottlesProduct from './icons/BottlesProduct.vue'
</script>

<template>
  <div class="content-block">
    <h2 class="heading">Healthy skin starts with good ideas.</h2>
    <p class="description">
      Discover our innovative skincare line, meticulously crafted for even the most reactive and
      sensitive skin. Our vegan and cruelty-free formulas harness the power of natural, safe
      ingredients to gently soothe, balance, and strengthen your skin’s natural barrier. Experience
      the difference.
    </p>
    <button class="learn-more-btn">
      <CirclreImgDark />
      Learn more
    </button>
  </div>

  <div class="line"></div>

  <div class="product-block">
      <AllInOneYellow />

    <div class="product-description-block">
      <div class="produce-content-block">
        <h2 class="product-name">Your new all-in-one super power</h2>

        <p class="product-description">
          Discover our innovative skincare line, meticulously crafted for even the most reactive and
          sensitive skin. Our vegan and cruelty-free formulas harness the power of natural, safe
          ingredients to gently soothe, balance, and strengthen your skin's natural barrier.
        </p>

        <p class="product-description">
          Free from silicones, sulfates, mineral oil, parabens, PEGs, microplastics, and other
          potential irritants, our products deliver effective care without compromise.
        </p>

        <div class="tag-block">
          <p class="tag">Energy</p>
          <p class="tag">Immunity</p>
          <p class="tag">Stress relief</p>
          <p class="tag">Health</p>
        </div>
      </div>

      <div>
        <button class="buy-button">Shop Now</button>
      </div>

      <BottlesProduct class="product-descr-img-small" />
    </div>
  </div>
</template>

<style>
.content-block {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  gap: 20px;
}

.heading {
  color: rgb(22, 22, 22);
  font-family: 'Inter Tight';
  font-size: 48px;
  font-weight: 300;
  line-height: 110%;
  letter-spacing: 0%;
  text-align: center;
}

.description {
  color: rgb(22, 22, 22);
  font-family: 'Inter';
  font-size: 16px;
  font-weight: 400;
  line-height: 150%;
  letter-spacing: 0%;
  text-align: center;
  max-width: 644px;
}

.learn-more-btn {
  width: 110px;
  height: 22px;
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 12px;
  background-color: unset;
  border: unset;
  cursor: pointer;
  margin-bottom: 80px;
}

.line {
  border: 1px solid rgb(224, 217, 226);
  margin: 0 46px;
}

.product-block {
  display: grid;
  grid-template-columns: 1fr 1fr;

  margin: 65px 46px 120px 46px;
}

.product-description-block {
  display: flex;
  flex-direction: column;
  gap: 48px;
  padding: 0px 115px 0px 147px;
  margin-top: 43px;
  flex: none;
  order: 1;
  flex-grow: 1;
}

.produce-content-block {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  gap: 16px;
  padding: 0px;

  flex: none;
  order: 0;
  align-self: stretch;
  flex-grow: 0;
}

.product-name {
  color: rgb(22, 22, 22);
  font-family: 'Inter Tight';
  font-size: 36px;
  font-weight: 300;
  line-height: 130%;
  letter-spacing: 0.25%;
  text-align: left;
}

.product-description {
  color: rgb(22, 22, 22);
  font-family: 'Inter';
  font-size: 16px;
  font-weight: 400;
  line-height: 150%;
  letter-spacing: 0%;
  text-align: left;
}

.tag-block {
  display: flex;
  flex-direction: row;
  gap: 12px;
}

.tag {
  color: rgb(22, 22, 22);
  font-family: 'Inter';
  font-size: 14px;
  font-weight: 400;
  line-height: 150%;
  letter-spacing: 0.4%;
  text-align: left;
  border-radius: 50px;
  background: rgb(244, 241, 244);
  padding: 8px 12px 8px 12px;
}

.buy-button {
  color: rgb(22, 22, 22);
  font-family: Inter;
  font-size: 16px;
  font-weight: 400;
  line-height: 140%;
  letter-spacing: 0%;
  text-align: left;
  box-sizing: border-box;
  border: 1px solid rgb(22, 22, 22);
  width: 100%;
  height: 46px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 10;
  padding: 12px 10px 12px 10px;
  background: unset;
  cursor: pointer;
}

.buy-button:hover {
  background: #f3f1f4;
  transition: 0.2s;
}

.product-descr-img-small {
  width: 100%;
}
</style>
