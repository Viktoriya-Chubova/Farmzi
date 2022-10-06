<template>
   <div class="cards">
      <div class="cards__card" v-for="item in data" :key="item">
         <img :src="require(`../assets/images/news/${item.image}.jpg`)" class="cards__image">
         <div class="cards__info">
            <div class="cards__items">
               <p class="cards__dateBy">Date: <span class="cards__item">{{item.date}}</span></p>
               <p class="cards__dateBy">By: <span class="cards__item">{{item.author}}</span></p>
            </div>
            <p class="cards__name">{{item.name}}</p>
            <p class="cards__text">{{item.text}}</p>
            <Button>Read More</Button>
         </div>
      </div>
   </div>
</template>

<script>
import Button from './Button.vue';
   export default {
    props: {
        data: {
            type: Array,
            default: () => [] //возвращает пустой массив
        }
    },
    components: { Button }
}
</script>

<style lang="scss" scoped>
@import "../assets/layouts/index.scss";
.cards {
   display: flex;
   gap: 30px;
   margin-top: 50px;
   
   &__card {
      background-color: $liteGreen;
      
   }
   &__info{
      padding: 30px;
   }
   &__items{
      display: flex;
      gap: 20px;
      margin-bottom: 23px;
   }
   &__dateBy {
      color: $primary;

   }
   &__item{
      color: $grey;
      font-size: 15px;
   }

   &__name {
      margin-bottom: 18px;
      font-size: 25px;
      color: $primary;
      font-family: 'Playfair Display', serif;
   }

   &__text {
      margin-bottom: 45px;
      color: $grey;
      line-height: 26px;
   }
}

</style>