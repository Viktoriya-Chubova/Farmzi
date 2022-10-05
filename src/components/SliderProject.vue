<template>
  <div class="slider">
    <div class="slider__items" :style="{'margin-left': '-' +(100 *currentSlideIndex) + '%'}" >
       <div v-for="item in data" :key="item.id">
         <div class="slider__image">
            <img :src="require(`../assets/images/slider/${item.image}.jpg`)" alt="" />
         </div>
         <div class="slider__card">
            <SliderItem class="slider__item">Project: 
               <p class="slider__info">{{item.project}}</p>
            </SliderItem >
            <SliderItem class="slider__item">Client: 
               <p class="slider__info">{{item.client}}</p>
            </SliderItem>
            <SliderItem class="slider__item">Location: 
               <p class="slider__info">{{item.location}}</p>
            </SliderItem>
            
         </div>
       </div>
    </div>
  </div>
  <button class="slider__btn prev" @click="prevSlide">
      <img src="../assets/images/slider/btnPrev.svg" alt="">
   </button>
  <button class="slider__btn " @click="nextSlide">
      <img src="../assets/images/slider/btnNext.svg" alt="">
  </button>
</template>

<script>
import SliderItem from './SliderItem.vue';
export default {
    props: {
        data: {
            type: Array,
            default: () => [], //возвращает пустой массив
        },
        interval: {
            type: Number,
            default: 0
        }
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
    components: { SliderItem }
};
</script>

<style lang="scss" scoped>
   @import "../assets/layouts/index.scss";
.slider {
   max-width: 1140px;
   overflow: hidden;
   
   &__items {
      display: flex;
      transition: all ease .5s;
      position: relative;
      margin-bottom: 40px;
   }


   &__card{
      background-color: $primary;     
      position: absolute;
      
      bottom: 4px;  //исправить??
      padding: 50px;
   }
   &__item{
      margin-bottom: 20px;
   }
   
   &__info{
      font-size: 22px;
      font-family: 'Playfair Display', serif;
      font-weight: 400;
      color: $white;
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