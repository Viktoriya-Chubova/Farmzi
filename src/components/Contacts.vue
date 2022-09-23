<template>
   <div class="contact">
          <img
            class="contact__icon"
            src="../assets/images/icons/iconTel.png"
            alt=""
          />
          <div class="contact__info">
            <p class="contact__text">Call us:</p>
            <div class="contact__text white"><a href="tel:+0089458648">+00 89 458 648</a></div>            
          </div>
        </div>
</template>

<script>
   export default {
      name: 'Contact'
   }
</script>

<style lang="scss" scoped>
.contact {
   display: flex;
    align-items: center;   
    

  &__icon {
    margin-right: 20px;
  }

  &__info {
    font-size: 17px;   
  }

  &__text {
    padding: 0;
    margin: 0 0 5px 0;
    & a {
    color: #fff;
    text-decoration: none;
    }
  }  
}

</style>