<template>
  <div id="app">
   <h1>{{title}}</h1>
      
   <div id="photos">
   <img v-bind:src="cubes[number-1].url">    
      
    <p>Dobili ste broj {{cubes[number-1].name}}</p>

   </div>
    <button @click="cheking()"> Role </button>

  
  </div>
</template>

<script>

export default {
  name: 'app',
  data: function() {
    return{
      title:"Play cube",
      cubes:[
        { 
          value:1,
          name:'jedan',
          url:require('./assets/jedan.png'),
        },
        { 
          value:2,
          name:'dva',
          url:require('./assets/dva.png'),
          
                 },
         { 
          value:3,
          name:'tri',
          url:require('./assets/tri.png'),
                 }, 
        { 
          value:4,
          name:'cetri',
          url:require('./assets/cetri.png'),
        },
        { 
          value:5,
          name:'pet',
          url:require('./assets/pet.png'),
                 },
        { 
          value:6,
          name:'sest',
          url:require('./assets/sest.png'),
                  }
      ],
     number:1,
                
    }
    
  },
         methods:{
    cheking:function(){    
      this.number=Math.floor(Math.random()*6)+1;
      
}
}}
</script>

<style>
#app{ 
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  width: 500px;
  height: 500px;
  margin-left: 100px;
  padding: 50px;
 
  text-align: center;

}
p{
  font-size: 30px;
}
button{
  width: 150px;
  height: 50px;
  background-color: lightseagreen;
  margin:30px;
}
body{
    background-color: yellowgreen;
   
}
</style>