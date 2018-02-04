<template>
  <div>
    <!-- <componentA></componentA>
   <h1 v-text="hello"></h1> 
   <h2 v-html="hello2"></h2>
   <h2>{{num+1}}</h2>
   {{status ? 'success' : 'fail'}} -->
  <ul>
  <li v-for="(item,index) in items">
    {{item.name}}-{{item.price}}-{{index }}
  </li>
  </ul>
  <button v-on:click="addItem()">add</button>
  <a :href="baidu">baidu</a>
  <a v-if="partA">adds</a>
  <a v-else>toggle</a>
  </div>
</template>

<script>
//  import HelloWorld from './components/HelloWorld'
// import componentA from './components/a'
export default {
  // components:{componentA},
 data (){
   return {
     partA:true,
     baidu:'http://www.baidu.com',
    //  hello :'Hello world!!',
    //  hello2 :'<span>hello</span>',
    //  num:2,
    //  status:true,
     items:[
       {
         name:'apple',
         price:22
       },
       {
         name:'banana',
         price:23
       }
     ]
   }
 },
 methods : {
   addItem(){
     this.items.pop();
   }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
