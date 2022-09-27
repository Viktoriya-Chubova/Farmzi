<template>
  <div
    class="title"
    :class="{
      title_green: variant === 'green',
      title_white: variant === 'white',
    }"
  >
    <slot> </slot>
  </div>
</template>

<script>
export default {
  name: "Title",
  props: {
    variant: {
      type: String,
      default: "green",
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/layouts/index.scss";
.title {
  font-size: 48px;
  font-family: "Playfair Display", serif;
  font-weight: normal;
  color: $primary;
  margin-top: 10px;

  &_white {
    color: $white;
  }
  &_green {
    color: $primary;
  }
}
</style>