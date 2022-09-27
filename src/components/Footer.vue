<template>
   <div class="footer">
         <container>    
            <div class="footer__row ">
               <div class="footer__col ">
                  <h3 class="footer__title">Explore</h3>
                  <ul class="footer__list">
                     <li class="footer__item" v-for="(menu, index) in footerExploreList" :key="index">
                        <img class="footer__svg"  src="../assets/images/icons/Vector.svg" alt="">
                        <a href="" class="footer__link" :to="menu.path">{{menu.name}}</a>
                     </li>
                  </ul>
               </div>
               <div class="footer__col ">
                  <h3 class="footer__title">Information</h3>
                  <ul class="footer__list">
                     <li class="footer__item" v-for="(menu, index) in footerInformationList" :key="index">
                        <img class="footer__svg" src="../assets/images/icons/Vector.svg" alt="">
                        <a href="" class="footer__link" :to="menu.path">{{menu.name}}</a>
                     </li>
                  </ul>
               </div>
               <div class="footer__col ">
                  <h3 class="footer__title">Service</h3>
                  <ul class="footer__list">
                     <li class="footer__item" v-for="(menu, index) in footerServiceList" :key="index">
                        <img class="footer__svg" src="../assets/images/icons/Vector.svg" alt="">
                        <a href="" class="footer__link " :to="menu.path">{{menu.name}}</a>
                     </li>
                  </ul>
               </div>
               <div class="footer__col_farmzi">
                  <div class="footer__logo">
                     <img src="../assets/images/logo/logo.png" alt="" />
                  </div>
                  <div class="footer__text white">
                     <p>Lorem Ipsum is simply dummy text of the printing and typeset industry has been the industry's standard.</p>
                  </div>
                  <Contacts/>
               </div>
            </div>          
                   
         </container> 
         
      <div class="footer__foot">
            <p> &copy; 2022 design and developed by <a href="#">Brandbes</a>. Powered by <a href="#">Webflow</a>.</p>
         </div> 
   </div>
</template>



<script>
import Container from "@/components/Container.vue";
import Contacts from "./Contacts.vue";
export default {
   name: "Footer",
   components: {
    Container,
    Contacts
   },
   data(){
      return{
         footerExploreList:[
            {name: 'About us', path: '/'},
            {name: 'FAQ', path: '/'},
            {name: 'Press & Blog', path: '/'},
            
         ],
         footerInformationList:[
            
            {name: 'Style Guide', path: '/'},
            {name: 'Change Log', path: '/'},
            {name: 'License', path: '/'},
            
         ],
         footerServiceList:[           
            {name: 'Flower', path: '/'},
            {name: 'Planting', path: '/'},
            {name: 'Watering', path: '/'},
         ]
      }
   }
};
</script>
