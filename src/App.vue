<template>

  <div id="app">
<!-- <Search/> -->
        <Nav/> 
    <div class="container ml-10 mb-16">

        <div class="mx-40">

          <AddTweet/>

        </div>

    </div>
    <div>
       <Footer/>
    </div>
   
  </div>
</template>

<script>
import Footer from './components/Footer.vue'
import Nav from './components/Nav.vue'
import AddTweet from './components/AddTweet.vue'
export default {
  name: 'App',
  components: {
    AddTweet,
    Nav,
    Footer
  }
}
</script>

<style src="./assets/css/tailwind.css">

</style>
