<template>
  <div class="card" @click="navigateToPosts">
    <div class="container">
      {{computedSubreddit}}
      <h2>{{subreddit}}</h2>
    </div>
  </div>
</template>

<script>
    
export default {
  props:['subreddit', 'image', 'date', 'upvotes', 'link'],
  methods:{
    navigateToPosts() {
      this.$router.push('/posts/r/' + this.computedSubreddit)
    }
  },
  computed: {
    computedSubreddit() {
      return this.subreddit.slice(2)
    }
  }
}
</script>

<style scoped>
  .card {
  /* Add shadows to create the "card" effect */
  margin-top: 3em;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  width:70%;
  margin-left: 5em;
}

/* On mouse-over, add a deeper shadow */
.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

/* Add some padding inside the card container */
.container {
  padding: 2px 16px;
  background-color: var(--countries--color--light);
}

.container h4{
    text-align:center;
}


@media (min-width:1024px) { 
 .card{
        width: 90%;
        margin-left: 2em;
  }
  
  /* .container{
    width:91%;
  } */
}

</style>