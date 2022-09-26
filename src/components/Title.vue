<template>
   <div class="title">
      <slot>

      </slot>
   </div>
</template>

<script>
   export default {
      
   }
</script>

<style lang="scss" scoped>
      @import "../assets/layouts/index.scss";
.title{
   font-size: 48px;
   font-family: 'Playfair Display', serif;
   font-weight: normal;
   color: $primary;
   margin-top: 10px;
}
</style>