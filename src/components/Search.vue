<template>
    <div id="app">
<div class="search-wrapper">
    <input type="text" v-model="search" placeholder="Search title.."/>
        <label>Search title:</label>
  </div>
</div>
</template>

<script>


export default {

  data() {
      return {

      }
   
  },
 computed: {
    filteredList() {
      return this.tweets.filter(tweet => {
        return tweet.toLowerCase().includes(this.search.toLowerCase())
      })
    }
  },
}
</script>

<style scoped>

</style>