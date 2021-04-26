<template>
    <div>
       <p v-html="rowHtml"></p>
        <h1>Home Component</h1>
        <h3 v-once>{{name}}</h3>
        <h3>{{name}}</h3>
        <h3>{{10+19}}</h3>
        <h3>{{a+b}}</h3>
        <h3>{{ok?"Yes":"NO"}}</h3>
        <button v-on:click="updateName">Name</button>
        <button v-bind:disabled="disableBtn" v-on:click="updateText">click</button>
 <!--    <users />
     <Products />-->
    </div>
</template>

<script>
//import users from './users'
//import Products from './Products'
export default {
    name:'Home',
  /*  components:{
        users,
        Products
    }*/
    data()
    {
        return {
            name: 'Ravi',
            a:10,
            b:20,
            //ok:true
            ok:false,
            rowHtml:"<h1>Template in use</h1>",//html in row
            disableBtn:false,
        }
    },
    methods:{
        updateText()
        {
            this.ok=!this.ok
        },
        updateName()
        {
            this.name="Peter"      
        }
    }
};

</script>
<style scoped>
    div{
        background-color: rgb(46, 119, 184);
        height:500px;
    }
</style>