<template>
  <div class="port-folio">
    <div class="port-folio__assets">
      <span class="port-folio__assets__label">나의 포트폴리오</span>
      <div class="port-folio__assets__total">
        <span class="label">총 평가액</span>
        <span class="valuation">$208,284.46</span>
      </div>
      <div class="port-folio__assets__bg"></div>
    </div>
    <div class="port-folio__detail">
      <div class="port-folio__detail__principal">
        <span class="label">투자원금</span>
        <span class="valuation">$169,380.32</span>
        <span class="revenue">(+38,904.14)</span>
      </div>
      <div class="port-folio__detail__return">
        <span class="label">수익률</span>
        <div class="data-box">
          <img src="@assets/icons/increase.svg" alt="" />
          <span class="data-box__rate">22.96%</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style lang="scss" scoped>
.port-folio {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  width: 420px;
  height: 350px;

  border-radius: 8px;
  border: 1px solid $color-gray-200;

  &__assets {
    position: relative;

    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: space-between;

    flex: 1;
    width: calc(100% - 36px);

    padding: 18px;

    background-image: url("src/assets/images/bg-1.png");
    border-radius: 8px 8px 0 0;

    &__label {
      font-size: 18px;
      font-weight: 600;

      color: $color-white-000;
    }
    &__total {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      justify-content: center;

      color: $color-white-000;

      .label {
        font-size: 16px;
        font-weight: 400;
      }
      .valuation {
        font-family: "Public Sans", sans-serif;
        font-size: 50px;
        font-weight: 700;

        z-index: 1;
      }
    }
    &__bg {
      position: absolute;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;

      width: 100%;

      background-image: url("src/assets/images/bg-2.png");
    }
  }
  &__detail {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;

    width: calc(100% - 36px);
    height: calc(130px - 44px);

    padding: 20px 18px 24px 18px;

    background-color: $color-white-000;
    border-radius: 0 0 8px 8px;

    &__principal {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      justify-content: center;

      .label {
        font-size: 16px;
        font-weight: 600;

        color: $color-gray-500;

        margin-bottom: 4px;
      }
      .valuation {
        font-family: "Public Sans", sans-serif;
        font-weight: 700;
        font-size: 30px;
      }
      .revenue {
        font-family: "Public Sans", sans-serif;
        font-weight: 700;
        font-size: 22px;

        color: $color-error-500;

        margin-left: 24px;
      }
    }
    &__return {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      justify-content: center;

      .label {
        font-size: 16px;
        font-weight: 600;

        color: $color-gray-500;

        margin-bottom: 2px;
      }
      .data-box {
        display: flex;
        align-items: center;
        justify-content: center;

        gap: 4px;

        &__rate {
          font-family: "Public Sans", sans-serif;
          font-weight: 700;
          font-size: 30px;
        }
      }
    }
  }
}
</style>
