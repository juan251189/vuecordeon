<template>
  <div class="faq">
    <div class="question">{{faq.question}}</div>
    <div class="answer">{{faq.answer}}</div>
  </div>
</template>

<script>
  export default{
    name:'FAQ',
    props:['faq','index']
  }
</script>
