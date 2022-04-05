<template>
<h1 @click="changeMessage">{{ msg }}</h1>
<h1>{{ reversedMessage }}</h1>
</template>

<script>
export default {
  data(){
    return {
      msg: 'Hello?'
    }
  },
  computed:{
    reversedMessage() {
         return this.msg.split('').reverse().join('')
      }
    },
    watch:{//변경사항을 감시
    msg(newValue){
      console.log('msg:', newValue)
    },
    reversedMessage(){
      console.log('reverseMessage: ', this.reversedMessage)
    }
    },
  methods: {
    changeMessage(){
      this.msg = 'Good!'
    }
    }
  }

</script>

<style scoped>

</style>