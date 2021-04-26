<template>
    <div>
        <h1 class="homestyle">Class and style bindings</h1>       
        <h1 v-bind:style="{color:'blue'}">Style bindings</h1> 
        <h1 v-bind:style="{color:colorKey}">Style bindings</h1>    
        <h1 v-bind:style="{display:true}">Class bindings with objects</h1>       
        <h1 v-bind:style="{display:show,displayColor:show}">Class bindings with objects</h1>     
        <h1 v-bind:class="[aryclass]">Class bindings with array</h1> 
         <h1 v-bind:class="[show?'yesShow':'noShow']">Class bindings with array</h1>   <!-- property defined -->     
    </div>
</template>


<script>
export default {
    name:'classnstyle',
    data()
    {
        return {
            //show:false
            show:true,//directly true and false can be used in display
            aryclass:'arrayclass',//proprety to be given for array class in property
            colorKey:'red'
        }
    }
};


</script>

<style scoped>
    .homestyle{
           background-color: orange;           
    }
    .display{
        background-color: brown;
    }
    .arrayclass{
         background-color: cyan;
    }
</style>