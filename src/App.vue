<template> 
 
  <div class="app">
    <Header></Header>    
    <main class="content"><router-view/></main>
    <Footer></Footer>
  </div>
</template>
<script>
  import Header from './components/Header.vue'
  import Footer from './components/Footer.vue'
  export default {  
    components: {
      Header,
      Footer,      
    }
}
</script>
<style lang="scss" scoped>
  .app{    
    height: 100vh; //vh-высотa области просмотра
    display: flex;
    flex-direction: column;
  }
  
  .content {
    flex: 1;
  }
  

</style>
