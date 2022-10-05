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
    <div class="team">
      <div class="team__rectangle"></div>
      <container class="team__container">
        <div class="team__title">
          <LineText class="team__lineText">Team Members</LineText> 
          <Title>Farmzi feel proud for skilled team members.</Title>  
        </div>
        <CardsTeam :data="TeamData" class="team__cards"></CardsTeam>
      </container>
    </div>
    <div class="video">
      <Container class="video__container">
        <div class="video__row">
          <div class="video__title">
            <LineText variant="green">Company intro video</LineText> 
            <Title variant="white">See our intro video and lets start your dream project.</Title>  
          </div>
          <div class="video__img">
            <img src="../assets/images/video.jpg" alt="">
          </div>
        </div>
      </Container>
    </div>
    <div class="statistics">
      <container class="statistics__container">
        <CardsStatistics :data="StatisticsData" class="statistics__cards"></CardsStatistics>
      </container>
    </div>
    <div class="slider">
      <container>
        <SliderProject :data="SliderData" :interval="2000"></SliderProject>
      </container>
    </div>
    <div class="review">
      <container>
        <div class="review__title">
          <LineText>Happy Clients</LineText> 
          <Title>Farmzi got best feedback from happy clients</Title>  
        </div>
        <ReviewClients :data="ReviewData"></ReviewClients>
        <CardList></CardList>
      </container>
    </div>
    <div class="news">
      <container>
        <div class="news__title">
          <LineText>Latest News</LineText> 
          <Title>Check now latest tips and tricks of gardening and landscaping from blog.</Title>  
        </div>
        <CardsNews :data="NewsData"></CardsNews>
      </container>
    </div>
    <div class="natural">
      <Container>
        <div class="natural__row">
          <img src="../assets/images/natural/natural1.png" alt="">
          <img src="../assets/images/natural/natural2.png" alt="">
          <img src="../assets/images/natural/natural3.png" alt="">
          <img src="../assets/images/natural/natural4.png" alt="">
          <img src="../assets/images/natural/natural5.png" alt="">
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
import Title from '@/components/Title.vue';
import {ServicesData, TeamData,StatisticsData, SliderData, ReviewData, NewsData} from '@/data/data.dummy'
import CardsServices from '@/components/CardsServices.vue'
import Contacts from '@/components/Contacts.vue';
import CardsTeam from '@/components/CardsTeam.vue';
import CardsStatistics from '@/components/CardsStatistics.vue';
import SliderProject from '../components/SliderProject.vue';
import ReviewClients from '../components/ReviewCard.vue';
import CardsNews from '../components/CardsNews.vue';

export default {
  name: 'Home',
  components: {
    Container,
    Button,
    LineText,
    Title,
    CardsServices,
    Contacts,
    CardsTeam,
    CardsStatistics,
    SliderProject,
    ReviewClients,
    CardsNews,
    
},
  data(){
    return{
      ServicesData: ServicesData,
      TeamData: TeamData,
      StatisticsData: StatisticsData,
      SliderData: SliderData,
      ReviewData: ReviewData,
      NewsData:NewsData
    }
  },
  
  
}
</script>

<style lang="scss" scoped>
  @import "../assets/layouts/index.scss";



</style>
