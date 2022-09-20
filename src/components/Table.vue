<template>
  
  <h1>couter</h1>
  <p>{{counter}} <sup>2</sup> = {{squereq}} </p>
  <p>{{counter}} <sup>2</sup> = {{squere()}} </p>

  <p>{{counter}} <sup>2</sup> = {{squereq}} </p>
  <p>{{counter}} <sup>2</sup> = {{squere()}} </p>

</template>

<script>


export default {
  name: 'MyTable',


  data(){
    return {counter: 5}
  },

  methods:{
  squere(){
 console.log('klk')
    return this.counter * this.counter
  }
    
},

computed:{

  squereq() {
     console.log('kkaka')
    return this.counter * this.counter
  }  
}

}


</script>

<style>

</style>