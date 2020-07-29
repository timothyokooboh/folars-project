<template>
  <div>
       <p>Works</p>
  </div>
</template>




<script>



export default {
  data(){
    return {
      name:this.$route.params.subreddit,
      subreddit: '',
    }
  },
  methods:{

  },
  mounted : function() {
    console.log("Mounted!")
  },

}
</script>

<style scoped>
    
</style>


