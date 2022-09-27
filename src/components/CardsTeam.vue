<template>
   <div class="cards" >
      <div class="cards__card" v-for="item in data" :key="item.id">         
         <img :src="require(`../assets/images/team/${item.image}.jpg`)" class="cards__image">
         <LineText><div>{{item.lineText}}</div></LineText>
         <div class="cards__name">{{item.name}}</div>
         <p class="cards__text">{{item.text}}</p>         
      </div>
   </div>
</template>
 
<script>

import LineText from '@/components/LineText.vue'
   export default {
    props: {
        data: {
            type: Array,
            default: () => [] //возвращает пустой массив
        }
    },
    components: { 
      LineText 
   }
}
</script>

<style lang="scss" scoped>
@import "../assets/layouts/index.scss";
.cards {
   display: flex;
   justify-content: space-between;
   

   &__image {
      margin-bottom: 29px;
   }
   &__name{
      margin-top: 5px;
      font-family: 'Playfair Display';
      color: $primary;
      font-size: 26px;
      margin: 10px 0 18px 0;
   }
   &__text {
      font-size: 15px;
      color: $grey;
      line-height: 26px;
      max-width: 300px;
   }
}

</style>