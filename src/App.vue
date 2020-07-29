<template>
  <div id="app">
      <router-view></router-view>
  </div>
</template>

<script>
import Home from "@/views/Home.vue"
export default ({
   components:{
    Home
   }
})
</script>

<style>
body{
  background-color: hsl(207, 26%, 17%);
  color: white;
  font-family: 'Amaranth', sans-serif;
}
</style>
