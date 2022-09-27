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
    <div class="service">
      <Container>
        <div class="service__title">
          <LineText class="service__lineText">Our Services</LineText> 
          <Title>Farmzi always provide amazing gardening and landscaping services.</Title>  
        </div>
        <CardsServices :data="ServicesData" class="service__cards"></CardsServices>
        <Button class="service__btn" variant="green">More Service</Button>
      </Container>
    </div>
    <div class="call">
      <Container>
        <div class="call__row">
          <div class="call__title">
            <LineText variant="green">Call To Action</LineText> 
            <Title variant="white">If you need any gardening service, you can contact with Farmzi.</Title>  
          </div>
          <div class="call__contacts">
            <Contacts class="call__contact"></Contacts>
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
import {ServicesData} from '../data/data.services'
import CardsServices from '../components/CardsServices.vue'
import Contacts from '../components/Contacts.vue';
export default {
  name: 'Home',
  components: {
    Container,
    Button,
    LineText,
    Title,
    CardsServices,
    Contacts
},
  data(){
    return{
      ServicesData: ServicesData
    }
  },
  
  
}
</script>

<style lang="scss" scoped>
  @import "../assets/layouts/index.scss";

</style>
