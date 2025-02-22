<script setup>
import Logo from './icons/LogoVue.vue'
import SearchIcon from './icons/SearchIcon.vue'
import ProfileIcon from './icons/ProfileIcon.vue'
import CartIcon from './icons/CartIcon.vue'

defineProps({
  msg: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div class="header-block">
    <Logo class="logo" />

    <div class="buttons-block">
      <button class="header-button">Shop</button>
      <button class="header-button">Subscribe</button>
      <button class="header-button">Ingredients</button>
      <button class="header-button">Blog</button>
    </div>

    <div class="header-icons-block">
      <SearchIcon />
      <ProfileIcon />
      <CartIcon />
    </div>
  </div>
</template>

<style scoped>
.header-block {
  box-sizing: border-box;
  border-bottom: 1px solid rgb(255, 255, 255);

  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  gap: 48;
  padding: 0px 46px 0px 46px;

  background: gray;
}

.logo {
  box-sizing: border-box;
  border-right: 1px solid rgb(255, 255, 255);
  width: 208px;
  height: 56px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 0px 48px 0px 0px;
}

.buttons-block {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  gap: 32px;
  padding: 10px 0px 10px 0px;

  flex: none;
  order: 0;
  flex-grow: 1;
  margin: 0px 10px;
}

.header-button {
  color: rgb(255, 255, 255);
  font-family: 'Inter';
  font-size: 16px;
  font-weight: 400;
  line-height: 140%;
  letter-spacing: 0%;
  text-align: left;
  cursor: pointer;
  background: none;
  border: none;
}

.header-icons-block {
  display: flex;
  flex-direction: row;
  gap: 12px;
  align-items: center;
}
</style>
