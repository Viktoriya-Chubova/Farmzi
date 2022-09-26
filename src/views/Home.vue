<template>
  <div class="home">   
    <div class="garden">
      <Container>      
        <div class="garden__row">
          <div class="garden__left">          
            <LineText variant="green">Make a garden with musion.</LineText>    
            <Title class="garden__title">If you have a garden and a library, you have everything you need.</Title>      
            
            <LineText variant="green">Marcus Tullius Cicero</LineText>
            <Button class="garden__btn">All Services</Button>
          </div>
          <div class="garden__right">
            <img src="../assets/images/home.jpg" alt="">
          </div>  
        </div>   
      </Container>
    </div>
    <div class="about">
      <Container>
          <div class="about__title">
            <LineText class="about__lineText">About Company</LineText> 
            <Title>Farmzi have 35 years of experience and know smart way to grow and design your beautiful garden.</Title>  
          </div>
          <div class="about__row">
            <div class="about__left">
              <img src="../assets/images/about.jpg" alt="">
            </div>
            <div class="about__right">
              <div class="about__subtitle">Who we are?</div>
              <p class="about__text">Lorem Ipsum is simply dummy text of the printing and typeset industry. Lorem Ipsum has been the industry's standard dumm ever since the 1500s, when an unknown printer took a galley scrambled it make a type specimen book.</p>
              <p class="about__quote">“Lorem Ipsum is simply dummy text of the printn industry lorem epsum has been the industry and scrambled it make a type specimen book”.</p>
              <div class="about__subtitle">Mission and vision</div>
              <p class="about__text">Lorem Ipsum is simply dummy text of the printing and typeset industry. Lorem Ipsum has been the industry's standard dumm ever since the 1500s, when an unknown printer took a galley scrambled it make a type specimen book.</p>
              <p class="about__text">Lorem Ipsum is simply dummy text of the printing and typeset industry. Lorem Ipsum has been the industry's standard dumm scrambled it make a type specimen book.</p>
              <Button class="about__btn">Learn More</Button>
            </div>
          </div>
      </Container>
    </div>
  </div> 
</template>

<script>
// @ is an alias to /src

import Container from '@/components/Container.vue'
import Button from '@/components/Button.vue'
import LineText from '@/components/LineText.vue'
import Title from '../components/Title.vue';
export default {
  name: 'Home',
  components: {
    Container,
    Button,
    LineText,
    Title
},
  
}
</script>

<style lang="scss" scoped>
  @import "../assets/layouts/index.scss";

  .garden {
    background-color: $primary;
    max-height: 788px;
    
    

    &__row{      
      display: flex;
      
    }
    
    &__title {      
      font-size: 60px;
      color: $white;
      margin: 19px 0 16px 0 ;
      padding: 0 95px 0 0;  
       
    }
    
    &__right img{
      margin-top: -44px;
    }
    &__btn{
      margin-top: 60px;
    }
  }



.about {
  padding-top: 115px;

  &__title {
    padding-right: 143px;
    
  }

  &__row {
    display: flex;
  }


  &__right {
    padding: 73px 0 73px 120px ;
  }
  &__subtitle,
  &__quote{
    font-family: 'Playfair Display', serif;    
    color: $primary;
  }
  &__subtitle {
    font-size: 32px;   
    
  }

  &__text {
    color:$grey;
    line-height: 26px;
    margin: 26px 0 15px 0;
  }

  &__quote {
    font-size: 22px;
    margin-bottom: 36px;
  }

  &__btn {
    margin-top: 75px;
  }
}

</style>
