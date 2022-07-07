<template>
<div id="app">
  
  <div class="container">
    <HelloWorld> </HelloWorld>
  </div>

</div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
  export default {
    components:{
      HelloWorld
    },
    data(){
      return{
        
      }
    }
  }
  
</script>

<style>
.container{
  font-family: Arial, sans-serif;
  font-size: 15px;
  max-width: 600px;
  background-color: #f5f5f9;
  border-radius: 7px;
  box-shadow: 0px 0px 12px #888;
  margin-top: 20px;
  padding: 20px 10px 10px;
  margin-right: auto;
}

</style>
