<template>
  <div
    class="lineText"
    :class="{
      lineText_green: variant === 'green',
      lineText_grey: variant === 'grey',
    }"
  >
    <div class="line"></div>
    <p class="text">
      <slot> </slot>
    </p>
  </div>
</template>

<script>
export default {
  name: "LineText",
  props: {
    variant: {
      type: String,
      default: "grey",
    },
  },
};
</script>


<style lang="scss" scoped>
@import "../assets/layouts/index.scss";
.lineText {
  display: flex;
  align-items: center;
  
  &_grey {
    .line {
      border-bottom: 1px solid $grey;
    }
    .text {
      color: $grey;
    }
  }
  &_green {
    .line {
      border-bottom: 1px solid $text;
    }
    .text {
      color: $text;
    }
  }
}
.line {
  width: 40px;  
  margin-right: 10px;
}
.text{
   font-size: 17px;
   margin: 0;
  padding: 0;
}
</style>
