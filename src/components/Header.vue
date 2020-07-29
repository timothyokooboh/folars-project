<template>
  <div class="header">
    <h1> Subreddits </h1>
</div>
</template>

<script>
export default {

    }

</script>

<style scoped>
  .header{
    display: flex;
    padding: 20px;
    background-color: hsl(209, 23%, 22%);
  }

  .header h1{
    margin-left: 0;
  }

  #dark{
    margin-left: 18em;
    height: 6em;
    width: 10%;
    margin-top: 3em;
  }

  .header h1{
    margin-left: .5em;
  }

@media (min-width:1024px) { 
  /* .header{
    padding: 3px;
  }

  .theme-switch-wrapper{
    margin-left: 45em;
  }

  h1{
    font-size: 1.1em;
  } */
}

</style>