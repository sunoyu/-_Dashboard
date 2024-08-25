<template>
  <div class="icon-button">
    <img
      :src="`src/assets/icons/${icon}.svg`"
      alt=""
      class="icon-button__image"
    />
    <img
      :src="`src/assets/icons/${icon}-hover.svg`"
      alt=""
      class="icon-button__image-hover"
    />
    <span class="icon-button__label">{{ label }}</span>
  </div>
</template>

<script setup lang="ts">
import { toRefs } from "vue";
interface Props {
  icon: string;
  label: string;
}

const props = defineProps<Props>();
const { icon, label } = toRefs(props);
</script>

<style scoped>
.icon-button {
  display: flex;
  align-items: center;
  justify-content: flex-start;

  width: calc(100% -16px);

  padding: 12px 18px;
  gap: 16px;

  &__image-hover {
    display: none;
  }
  &__label {
    font-weight: 500;
    font-size: 19px;

    color: $color-gray-500;
  }
  &:hover {
    background-color: $color-gray-100;
    border-radius: 4px;

    .icon-button__label {
      color: $color-gray-900;
    }
    .icon-button__image {
      display: none;
    }
    .icon-button__image-hover {
      display: block;
    }
  }
}
</style>
