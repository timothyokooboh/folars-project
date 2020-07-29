<template>
  <div>
    <input 
      name="value" 
      v-model= "reddit" 
      placeholder="Search for a subreddit...."
    >
  </div>
</template>

<script>
export default {
  data(){
    return{
      reddit: ''
    }
  },
  methods:{

  }
          
}
</script>

<style scoped>
     input{
    background-color:hsl(209, 23%, 22%);
    padding: 10px;
    padding-left: 3em;
    color:white;
    margin-top: 1em;
    margin-left: 2em;
    width: 70%;
    height: 3em;
    border-radius: .5em;
    font-size: 1.2em;
    outline: none;
    border: 1px solid hsl(207, 26%, 17%);
  }

  
@media (min-width:1024px) { 

}
</style>


