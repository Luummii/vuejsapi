<template>
  <div class="example">
    <p v-text="msg_1"></p>    
    <p v-text="msg_2"></p>    
    <p v-text="msg_3"></p>    
    <p>{{ msg_4 }}</p>    
    <p>{{ msg_5 }}</p>    
    <p>{{ msg_6 }}</p>    
    <p>{{ msg_7 }}</p>    
  </div>
</template>

<script>
export default {  
  data () {
    return {
      msg_1: 'Использование v-text="message"',
      msg_2: 123,
      msg_3: true,
      msg_4: '<div>ASD</div>',
      msg_5: [],
      msg_6: null,
      msg_7: undefined,
    }
  }
}
</script>

<style lang="stylus" scoped>
</style>