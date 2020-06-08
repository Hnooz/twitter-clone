<template>

  <div id="app">
<!-- <Search/> -->
        <Nav/> 
    <div class="container ml-10">

        <div class="mx-40">

          <AddTweet/>

        </div>

    </div>
    
  </div>
</template>

<script>
// import Search from './components/Search.vue'
import Nav from './components/Nav.vue'
import AddTweet from './components/AddTweet.vue'
export default {
  name: 'App',
  components: {
    AddTweet,
    Nav,
    // Search
  }
}
</script>

<style src="./assets/css/tailwind.css">

</style>
