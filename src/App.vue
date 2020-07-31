<template>
<div id="app">
  <header>
    <h1>Vue<span>CORDION</span></h1>
  </header>
  <div class="faqs">
    <FAQ v-for="(faq,i) in faqs" :faq="faq" :index="i" :key="i">
    </FAQ>
  </div>

</div>
</template>

<script>
import FAQ from './FAQ';

export default {
  name: 'App',
  components: {
    FAQ
  },
  data() {
    return {
      faqs: [{
          question: 'where are you from?',
          answer: 'Colombia',
          open: false

        },
        {
          question: 'how long have you been here?',
          answer: 'Colombia',
          open: false
        },
        {
          question: 'are you studing?',
          answer: 'Colombia',
          open: false
        }
      ]
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background-color: #EEE;
  font-family: sans-serif;
}

header {
  background-color: #3c3c3c;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 15px;
}

header h1 {
  color: #EEE;
  font-size: 28px;
  font-weight: 300;
  text-transform: uppercase;
}

header h1 span {
  color: #56e3b8;
  font-weight: 900;
}

.faq{
  display:block;
  width: 100%;
  max-width: 768px;
  margin: 15px auto;
  padding:15px;
  border-radius: 8px;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.25);
  background-color: #fff;

}

.faq .question{

  position:relative;
  color:#3c3c3c;
  font-size: 20px;
  transition: all 0.4s linear;
}

.faq .question::after{
  content: '';

  position: absolute;
  top:50%;
  right: 0px;
  transform: translateY(-50%) rotate(0deg);

  width: 30px;
  height: 30px;
  background-image: url('./arrow-down-mint.svg');
  background-position: center;
  background-size: contain;
  background-repeat: no-repeat;

}
</style>
