<template>
  <div class="page">
    <!-- 네비게이션 ui -->
    <Navigaion></Navigaion>
    <div class="page__container">
      <!-- 헤더가 들어가는 부분 -->
      <Header></Header>
      <div class="page__container__contents">
        <div class="summary">
          <!-- 포트폴리오 ui -->
          <PortFolio></PortFolio>
          <!-- 차트 -->
        </div>
        <div class="table">
          <!-- 테이블이 들어가는 부분 -->
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import Header from "@components/organisms/common/Header.vue";
import Navigaion from "@components/organisms/common/Navigation.vue";
import PortFolio from "@/components/molecules/main/PortFolio.vue";
</script>

<style lang="scss" scoped>
.page {
  display: flex;
  align-items: center;
  justify-content: center;

  width: 100%;
  height: 100vh;

  &__container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    width: 1440px;
    height: calc(100% - 48px); // 전체 100vh 에서 48px(padding)

    padding: 24px 48px 24px 32px; // top right bottom left

    background-color: $color-gray-100;

    &__contents {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: flex-start; // 위에서 아래로

      width: 100%;
      flex: 1; // 높이를 안줘도 꽉채워서 사용하게 된다.

      margin-top: 50px;
      gap: 24px;

      .summary {
        display: flex;
        align-items: center;
        justify-content: space-between; // 부모태그으 ㅣ양쪽 끝에 붙이는

        width: 100%;
        gap: 24px;
      }
      .table {
        display: flex;
        align-items: center;
        justify-content: center;

        width: 100%;
        height: calc(100vh - 532px);
      }
    }
  }
}
</style>
