<template>
  <div id="app">
    <header>
      <h1>Vue<span>CORDION</span></h1>
    </header>

  </div>
</template>

<script>
import FAQ from './FAQ';

export default {
  name: 'App',
  components:{
    FAQ
  },
  data(){
    return{
      faqs:[{
        question:'',
        answer:'',
        open:false

      }]
    }
  }
}
</script>

<style>


*{
  margin:0;
  padding: 0;
  box-sizing: border-box;
}

body{
  background-color: #EEE;
  font-family: sans-serif;
}

header{
  background-color: #3c3c3c;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 15px;
}
header h1{
  color:#EEE;
  font-size: 28px;
  font-weight: 300;
  text-transform: uppercase;
}

header h1 span{
  color:#56e3b8;
  font-weight: 900;
}
</style>
