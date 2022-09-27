<template>
   <div class="cards" >
      <div class="cards__card" v-for="item in data" :key="item.id">         
         <img :src="require(`../assets/images/${item.image}.jpg`)" class="cards__image">
         <LineText><div>{{item.lineText}}</div></LineText>
         <p class="cards__title">{{item.title}}</p>         
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

   &__title {
      margin-top: 5px;
      font-family: 'Playfair Display';
      color: $primary;
      font-size: 22px;
      
   }
}

</style>