<template>   
      <button class="btn" 
      :class="{
         'btn_white': variant === 'white',
         'btn_green': variant === 'green'
      }">
         <slot> 

         </slot>
         <img class="btn__img" src="../assets/images/icons/button.svg" alt="">
      </button>
  
</template>

<script>
   export default {
      name: 'Button',

      props:{
         variant:{
            type: String,
            default: 'white'
         }
      }
   }
   
</script>

<style lang="scss" scoped>
   @import "../assets/layouts/index.scss";
.btn{
      
      color: $primary;
      border: 2px solid $primary;
      padding: 9px 52px ;
      line-height: 26px;
      

      &:hover{
         box-shadow: 0 0 10px rgba(0,0,0,0.5);
      }
      &__img{         
         padding-left: 10px;
      }
      &_white{
         background-color: $white;
      }

      &_green{
         background-color: $liteGreen;
      }

   }
   

</style>