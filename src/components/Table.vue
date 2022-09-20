import { title } from 'process';
<template>
  
  <h1>{{changes }}</h1>
  <p>{{counter}} <sup>2</sup> = {{squere()}} </p>
  <p>{{name}}</p>
  
  <div>
    <button class="bto" v-on:click="incremetar">+1</button>
    <button class="bto" v-on:click="descre">-1</button>
    <button class="bto" v-on:click="change">name</button> 
  </div>
  

</template>

<script>


export default {


  name: 'MyTable',
  props: {
    title: String,
    counters: {
      type: Number,
      default: 100,
      //required: true,
      validator(value){
        return value > 100
      }

    }

  },

  data(){
    return {counter: this.counters, name: 'alfredo'}
    
  },

  methods:{
  squere(){
    return this.counter * this.counter
  },

  incremetar(){
    return this.counter++
  },
  descre(){
    return this.counter--
  },

  change(){
    this.name = 'Elias'
  }
    
},

computed:{

  squereq() {
     console.log('kkaka')
    return this.counter * this.counter
  } ,
  
  changes(){
       
    return this.title || this.name
      
  }
}

}

</script>

<style>
 
 .bto{

  background-color: aquamarine;
  border-radius: 1px solido #fff;
  margin: 0 5px;
  padding: 10px;

 }

 .bto:hover{
  background-color: antiquewhite;
 }

</style>