<template>
   <div class="cards">
      <div class="cards__card point" v-for="item in data" :key="item.id">
         <p class="cards__count">{{item.count}}</p>
         <LineText><div>{{item.lineText}}</div></LineText>
      </div>
   </div>
</template>

<script>
import LineText from './LineText.vue';
   export default {
      props: { 
        data: {
            type: Array,
            default: () => [] //возвращает пустой массив
        }
    },
    components: { LineText }
}
</script>

<style lang="scss" scoped>
@import "../assets/layouts/index.scss";

.cards {
   display: flex;
   justify-content: space-between;
   
   background-color: $liteGreen;
   
   /* ::after{
         content: '';
         background-color: $primary;
         width: 4px;
         height: 7px;
         
      } */
   &__card {
      margin: 64px auto;
      
      
   }

   &__count {
      text-align: center;
      font-size: 45px;
      color: $primary;
      line-height: 73px;
   }
}


</style>