<template>
  <div>
    <Header />
    <Search @reddit="getRedditValue($event)"/>
    <Filtered />
    <Subreddits 
      v-for="(item, index) in info" 
      :key="index" 
      :subreddit="item.data.subreddit_name_prefixed"
    />
  </div>
</template>

<script>
// @ is an alias to /src
import Header from "@/components/Header.vue";
import Search from "@/components/Search.vue";
import Filtered from "@/components/Filtered.vue";
import Subreddits from "@/components/Subreddits.vue";
import Posts from './Posts.vue';



export default {
    data(){
        return{
            info:[],
            search:''
        }
    },   
 methods:{
     
    },
    mounted () {
      //  axios
      // .get(`https://www.reddit.com/.json`)
      // .then(response => {
      //     const returnedData = this.info = response.data.data.children.map(data => data.data)
      //     var parsedData = JSON.parse(JSON.stringify(returnedData))
      //     console.log(parsedData)
      // .catch (err => console.log(err));
      // })
      axios.get("https://www.reddit.com/.json")
      .then((res) => {
        console.log(res.data)
        this.info = res.data.data.children
      })
      .catch((err) => console.log(err))
},
  name: "Home",
  components: {
    Header,
    Search,
    Filtered,
    Subreddits
  },
    computed: {
      Subreddits: function(){ 
        return this.parsedobj.filter((subreddit) => {
         
        })
      },
    }
};
</script>
