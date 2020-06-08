<template>

  <div class="">
    
    <div class="">

          <div :class="show() ? 'mt-10' : 'mb-10 mt-10'">
            <label class="font-semibold pr-6 py-2 text-gray-700">Search tweet:</label>
            <input type="text" class="bg-gray-400 placeholder-gray-700 text-gray-700 pl-2 py-2 rounded" v-model="search" placeholder="Search tweet.."/>
              
          </div>

          <div  v-show="show()">
              <h1 class="font-medium pt-10 text-2xl text-gray-700">Add Tweet</h1>

              <textarea class="bg-gray-400 h-40 mt-16 pl-5 placeholder-gray-700 pt-5 rounded-lg text-gray-700 w-full" placeholder="type what you think about..." v-model="newTweet"></textarea>

              <input type="submit" value="Add Tweet" @click="addTweet"  class="bg-gray-700 block font-semibold mb-8 mt-6 px-10 py-3 rounded-lg text-blue-400" :disabled="newTweet.length >= 60 || newTweet == ''? true : false">

          </div>
        
          <ul class="text-white">
            <li   v-for="tweet of filteredList" :key="tweet.index" class="mb-10">
              <p class="bg-gray-700 border-b-2 border-blue-300 mb-10 px-5 py-10 rounded-lg">
                {{tweet}}
              </p>
              </li>
          </ul>

      </div>
  </div>
</template> 

<script>
// import Search from './components/Search.vue'
export default {
  name: 'AddTweet',
  components:{
    // Search
  },


  data() {
    return {
      search:'',
      newTweet:'',
      tweets:[
      'this is test',
      ],

    }
  },



  methods: {
    addTweet(){
      this.tweets.push(this.newTweet);
      this.newTweet ='';
    },
    show(){

    return  this.search.length == 0 ? true : false;

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

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
