<template>
  <div class="navbar">
    
      
        <div class="navbar__logo">
          <img class="navbar__img" src="../assets/images/logo/logo.png" alt="" />
        </div>
        <ul class="navbar__list">
          <li class="navbar__item" v-for="(menu, index) in headerMenuList" :key="index">
            <router-link href="" :to="menu.path">{{menu.name}}</router-link>
          </li>
          
        </ul>
        <Contacts class="navbar__contact"/>
      
    
  </div>
</template>

<script>

import Contacts from "./Contacts.vue";

export default {
  name: "Header",
  components: {
    
    Contacts
},
data(){
    return {
      headerMenuList:[
        {id: 1, name: 'Home', path: '/'},
        {id: 2, name: 'About', path: '/about'},
        {id: 3, name: 'Pages', path: '#'},
        {id: 4, name: 'Blog', path: '#'},
        {id: 5, name: 'Contact', path: '#'},
   
      ]
    }
  }
};
</script>

<style scoped lang="scss">
@import "../assets/layouts/index.scss";
.navbar {
  height: 107px;
  background-color: $primary;
  display: flex;    
    padding: 29px 60px;



  &__logo {
    margin-right: 236px;
  }

  &__list {
    display: flex;
    font-size: 15px;
    margin: 0;
    padding: 0;
    /* margin-right: 200px; */
    align-items: center;

    & a {
    color: $text;
    text-decoration: none;

    &:hover {
      color: #fff;
    }
  }
  }

  &__item {
    padding: 0;
    list-style-type: none;
    margin-right: 40px;
    text-align: center;

    &:last-child {
      margin: 0px;
    }
  }

  &__contact{
    margin-left: auto; // прибили к правому краю
  }
}


</style>
