<template>
  <div class="container">
      <NavBar :logo="logo_src" :alt="app_name"/>
    <div class="footerApp">
      <router-view/>
      <Footer />
    </div>
  </div>
  
</template>

<script>
  import NavBar from "./components/NavBar.vue"
  import Footer from "./components/Footer.vue"
export default {
  components:{
    NavBar,
    Footer
  },
  data(){
    return{
      logo_src: "/imgs/logo.png",
      app_name: "Make Your Burguer"
    }
  }
}
</script>


<style>

  *{
    font-family: helvetica;
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }

  .main-container{
    margin: 50px;
    min-height: 250px;
  }

  h1{
    text-align: center;
    font-size: 42px;
    margin-bottom: 30px;
    color: #222;
  }

  .container{
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

</style>
