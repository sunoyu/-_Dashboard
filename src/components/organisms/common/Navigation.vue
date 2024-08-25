<template>
  <div class="navigation">
    <img
      src="@assets/images/logo.png"
      alt=""
      class="navigation__logo"
      @click="toHome"
    />
    <div class="navigation__menu-box">
      <div class="navigation__menu-box__top">
        <!-- V-for 로 변환해보기 -->
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
import router from "@/routes";
function toHome() {
  router.push({ path: "/", name: "home" });
}
</script>

<style scoped>
.navigation {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: space-between;

  width: calc(312px - 80px);
  height: calc(100% - 104px);

  padding: 24px 40px 80px 40px;

  border-right: 1px solid $color-gray-200;
  border-left: 1px solid $color-gray-200;

  background-color: $color-white-000;

  &__logo {
    cursor: pointer;
  }
  &__menu-box {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: space-between;

    width: 100%;
    height: 100%;

    margin-top: 52px;

    &__top {
      display: flex;
      flex-direction: column;

      width: 100%;

      gap: 28px;

      .menu {
        width: 100%;
        text-decoration: none;
      }
    }
    &__bottom {
      display: flex;
      align-items: center;
      justify-content: flex-start;

      width: 100%;

      .menu {
        width: 100%;
        text-decoration: none;
      }
    }
  }
}
</style>
