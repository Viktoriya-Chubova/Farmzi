<template>
  <div class="home">   
    <div class="garden">
      <Container>      
        <div class="garden__row">
          <div class="garden__left">          
            <LineText variant="green">Make a garden with musion.</LineText>          
            <p class="garden__title white">If you have a garden and a library, you have everything you need.</p>
            <LineText variant="green">Marcus Tullius Cicero</LineText>
            <Button class="garden__btn">All Services</Button>
          </div>
          <div class="garden__right">
            <img src="../assets/images/home.jpg" alt="">
          </div>  
        </div>   
      </Container>
    </div>
    <div>
      <Container>
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Soluta assumenda similique blanditiis voluptate inventore repellendus officia molestias! Illo, qui! Alias aliquam quisquam minima impedit illo sint voluptas nulla repellendus? Nemo?
        Veritatis, est ipsa iste dolore nulla quos, tenetur optio reiciendis consequuntur suscipit at accusantium in ipsam quo, praesentium quia perspiciatis? Provident quos aliquam voluptates nihil cupiditate dolore ut quasi quidem.
        Ullam cum officia recusandae est odio fugiat mollitia nobis qui deserunt distinctio alias, laudantium animi nisi nemo optio laborum corrupti sunt saepe tenetur modi ipsa enim at. Suscipit, vitae ducimus!
        Itaque animi temporibus velit consequuntur accusantium. Suscipit quis ab incidunt nostrum dignissimos in rem obcaecati aspernatur. Velit pariatur sed nobis ut molestias eligendi corporis eos incidunt suscipit, minima quasi deleniti?
        Veniam corporis odio sunt est porro nulla ab voluptatibus! Provident veniam magnam, consectetur, quia quasi autem alias aperiam eum ipsa impedit facilis distinctio iure? Laudantium quae cupiditate error accusantium facilis?
        Pariatur debitis ex odit! Quisquam mollitia quidem velit. Similique impedit, dignissimos aliquam aut veniam sit quam modi excepturi fugiat tempore distinctio consectetur molestiae, quisquam, ex itaque nemo eaque nostrum accusantium.
        Nobis a quibusdam non. Minima corrupti itaque repellat hic excepturi cupiditate quibusdam, culpa architecto vero at sequi eius tempora quo ratione dicta ad harum obcaecati optio praesentium nam, consequatur iste.
        Ipsum praesentium tempore incidunt est quibusdam tempora cupiditate animi sit harum facilis, aliquid architecto consequatur? Aliquam fuga in optio provident ab molestiae, minus voluptates quisquam nemo porro, maxime doloribus ipsa.
        Molestiae veniam possimus sed quaerat est itaque officia? Laudantium, deleniti odit sint consequuntur natus asperiores nam qui quo enim eius dolore fugit illum nobis iste dolor repudiandae corrupti rerum tenetur!
        Quisquam eius ea fugit adipisci dolore quis officia consequuntur. Temporibus illo dolorum, alias saepe incidunt delectus quibusdam officiis voluptate perspiciatis quasi placeat molestiae quas ab iure eum sapiente sit possimus.
      </Container>
    </div>
  </div> 
</template>

<script>
// @ is an alias to /src

import Container from '@/components/Container.vue'
import Button from '@/components/Button.vue'
import LineText from '@/components/LineText.vue'
export default {
  name: 'Home',
  components: {    
    Container,
    Button,
    LineText
  },
  
}
</script>

<style lang="scss" scoped>
  @import "../assets/layouts/index.scss";

  .garden {
    background-color: $primary;
    max-height: 788px;
    padding: 100px 0;
    

    &__row{      
      display: flex;
      
    }
    &__left {
      padding: 0 15px;
      
    }

    &__title {
      
      font-size: 60px;
      font-family: 'Playfair Display', serif;
      font-weight: normal;
      margin: 0;
      padding: 0 95px 0 0;  
       
    }

    &__right {
      margin-top: -44px;
    }
    &__btn{
      margin-top: 60px;
    }
  }

</style>
