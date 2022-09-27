<template>
   <div class="footer">
         <container>           
            <div class="footer__row ">
              <FooterNav :data="FooterNavData"></FooterNav>
               <div class="footer__farmzi">
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
import FooterNav from "./FooterNav.vue";
import {FooterNavData} from '../data/data.dummy'
export default {
   name: "Footer",
   components: {
    Container,
    Contacts,
    FooterNav
},
data(){
    return{
      FooterNavData: FooterNavData
    }
  },
};
</script>
