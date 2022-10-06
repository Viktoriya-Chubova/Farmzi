<template>
   <div class="reviews" >
      <div class="reviews__items" :style="{'margin-left': '-' +(50 *(currentSlideIndex)) + '%'}">
         <div v-for="item in data" :key="item" >
            <div class="reviews__item">
               <p class="reviews__text">{{item.text}}</p>
               <LineText class="reviews__lineText"><div>{{item.lineText}}</div></LineText>
               <p class="reviews__author">{{item.author}}</p>
            </div>
         </div>
      </div>
   </div>
   <button class="reviews__btn prev" @click="prevSlide">
      <img src="../assets/images/slider/btnPrev.svg" alt="">
   </button>
  <button class="reviews__btn " @click="nextSlide">
      <img src="../assets/images/slider/btnNext.svg" alt="">
  </button>
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
   },
   data() {
        return {
            currentSlideIndex: 0,
        };
    },
    methods: {
        prevSlide() {
            if (this.currentSlideIndex > 0) {
                this.currentSlideIndex--;
            }
        },
        nextSlide() {
            if (this.currentSlideIndex >= this.data.length - 1) {
                this.currentSlideIndex = 0;
            }
            else {
                this.currentSlideIndex++;
            }
        },
    },
}
</script>


<style lang="scss" scoped>
   @import "../assets/layouts/index.scss";
.reviews {
   max-width: 1140px;
   overflow: hidden;
   
   &__items{
      width: 540px;
      display: flex;
      
      gap: 60px;
      transition: all ease .5s;
      position: relative;
      margin-bottom: 40px;
   }
   &__item {
      width: 540px;
      background-color: $white;
      padding: 60px;
      color: $primary;
      font-family: 'Playfair Display', serif;
      background-image: url(../assets/quot.png);
      background-repeat: no-repeat;
      background-position: 50% 10%;
   }

   &__text {
      margin-bottom: 70px;
      font-size: 22px;
   }
   &__lineText{
      margin-bottom: 15px;
   }
   &__author {
      font-size: 26px;
   }

   &__btn{
      width: 70px;
      height: 70px;
      border: 2px solid $text;
      background-color: $white;
      margin-right: 66px;
      &:hover{
         box-shadow: 0 0 10px rgba(0,0,0,0.5);
      }
   }
}
   </style>