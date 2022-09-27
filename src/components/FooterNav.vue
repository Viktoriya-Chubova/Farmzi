<template>
  <div class="footerNav">
    <div class="footerNav__col" v-for="item in data" :key="item.id">
      <p class="footerNav__title">{{ item.title }}</p>
      <ul class="footerNav__list">
        <li
          class="footerNav__item"
          v-for="(menu, index) in item.list"
          :key="index"
        >
          <img
            class="footerNav__svg"
            src="../assets/images/icons/Vector.svg"
            alt=""
          />
          <a href="" class="footerNav__link" :to="menu.path">{{ menu.name }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    data: {
      type: Array,
      default: () => [], //возвращает пустой массив
    },
  },
  components: {},
};
</script>

<style lang="scss" scoped>
@import "../assets/layouts/index.scss";
.footerNav {
   background-color: $primary;
   display: flex;
   justify-content: space-between;
   min-width: 600px; //исправить

 &__col {
    padding-top: 66px;
    margin-right: 20px;   
    
  } 

  &__title {
    font-family: "Playfair Display", serif;
    font-weight: normal;
    font-size: 30px;
    margin: 0 0 39px 0;
    color: $white;
  }

  &__list {
    list-style-type: none;
    font-size: 15px;
    padding: 0;
  }

  &__item {
    padding: 20px 0;
  }

  &__svg {
    margin-right: 18px;
  }
  &__link {
    text-decoration: none;
    color: $white;

    &:hover {
      color: $text;
    }
  }
}
</style>