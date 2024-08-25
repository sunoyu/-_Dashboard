<template>
  <div class="navigation">
    <img src="scr/assets/images/logo.png" alt="" class="navigation__logo" />
    <div class="navigation__menu-box">
      <div class="navigation__menu-box__top">
        <RouterLink to="/" class="menu">
          <IconButton :icon="'folder'" :label="'내 포트폴리오'"></IconButton>
        </RouterLink>
        <RouterLink to="/about" class="menu">
          <IconButton :icon="'chart'" :label="'종목 검색기'"></IconButton>
        </RouterLink>
      </div>
      <div class="navigation__menu-box__bottom"></div>
    </div>
  </div>
</template>

<script setup lang="ts">
import IconButton from "@/components/atoms/buttons/IconButton.vue";
</script>

<style scoped></style>
