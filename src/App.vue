<template>

<div id="app">
  
  <div class="container">
    <HelloWorld> </HelloWorld>
    <hr>
  </div>

</div>
<div class="container2">
  <h1>parent componenet(User)</h1>
  <p>Buras� parent component her �eyin import edildi�i componenett</p>
  <button @click="changeName">Degistir</button>
  <p>child den gelen veri:{{chilData}} </p>


  <hr>
  <div class="row">

    <div class="child1">
      <childOne  @data="chilData=$event" :name="title"></childOne>
    </div>

    <div class="child2">
      <childTwo ></childTwo>
    </div>

  </div>

</div>




<div class="container">
  <button @click="selectedComponent='MemoryComponent'">MemoryComponent</button>
  <button @click="selectedComponent='NewMemoryComponent'">NewMemoryComponent</button>
  <button @click="selectedComponent='AuthorComponent'">AuthorComponent</button>
 
 <keep-alive>
  <component :is="selectedComponent">
  </component>
  </keep-alive>
  <!-- <MemoryComponent>
    <h1>BAslik</h1>
    <p>Slot kullanimi</p>
  </MemoryComponent> -->
</div>
</template>






<script>

import HelloWorld from './components/HelloWorld.vue'
import ChildOne from './components/ChildOne.vue'
import ChildTwo from './components/ChildTwo.vue'
import MemoryComponent from './components/MemoryComponent.vue'
import NewMemoryComponent from './components/NewMemoryComponent.vue'
import AuthorComponent from './components/AuthorComponent.vue'
  export default {
    components:{
    HelloWorld,
    ChildOne,
    ChildTwo,
    MemoryComponent,
    // eslint-disable-next-line vue/no-unused-components
    NewMemoryComponent,
    // eslint-disable-next-line vue/no-unused-components
    AuthorComponent
},
    data(){
      return{
        title:"Serif",
        chilData:"",
        selectedComponent:""
      }
    },
    methods:{
      changeName(){
        this.title="Sezen"
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
.container2{
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
.row{
  display:flex;
  align-items: center;
  justify-content: space-between;
}
.child1{
  background-color: #cacacc;
  margin-right: 5px;
}
.child2{
  background-color: #959597;
}
button{
  margin:5px;
}
</style>
