<template>
  <div id="app">
  <!--<Home />-->
  <!--<classnstyle />-->
  <!--<DataBind />-->
   <h1>Props in Vue js</h1>
   <!--For child component-->
   <Child1 name="Aki" />
   <!--<Child name=userName /> not working-->
   <Child1 v-bind:name="userName" /><!--for code:11-->
    <Child1 v-bind:users="users" /><!--for code:12-->
    <Child2 />
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
//import Home from './components/Home'
//import classnstyle from './components/classnstyle'
//import DataBind from './components/DataBind'
import Child1 from './components/Child1'
import Child2 from './components/Child2'
export default {
  name: 'App',
  components:{
    //classnstyle,
    //HelloWorld
   // Home,
   //DataBind,
   Child1,
   Child2,
  },
  data(){//this is for chil component
        //return {userName:"AK"}//for code:11
        return {users:[//for code:12
          {name:"AK1",email:"AK1@gmail.com"},
           {name:"AK2",email:"AK2@gmail.com"},
            {name:"AK3",email:"AK3@gmail.com"}
        ]}
  }
};


</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
