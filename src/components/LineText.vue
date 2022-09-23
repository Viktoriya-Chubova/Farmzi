<template>
  <div class="lineText">
     <div class="line" 
      :class="{
         'line_green': variant === 'green',
         'line_grey': variant === 'grey',      
      }">
      
     </div>   
     <p>
        <slot>

        </slot>
     </p>
  </div>
</template>

<script>
export default {
  name: "LineText",
  props:{
   variant:{
      type: String,
      default: 'grey'
   }
  }
};
</script>


<style lang="scss" scoped>
   @import "../assets/layouts/index.scss";
   .lineText{
      display: flex;
      align-items: center;   
      
   }
   .line{
      width: 40px;
      border-bottom: 1px solid $text;
      margin-right: 10px;
      
         &_grey{
            border-bottom: 1px solid $grey;
         }
         &_green{
            border-bottom: 1px solid $text;
         }
      }
   


</style>
