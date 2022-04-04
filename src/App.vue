<template>
<h1>{{ reversedMessage }}</h1>
<h1>{{ reversedMessage }}</h1>
<h1>{{ reversedMessage }}</h1>
<h1>{{ reversedMessage }}</h1>
</template>

<script>
export default {
  data(){
    return {
      msg: 'Hello Computed!'
    }
  },
  computed:{
    reversedMessage(){
      return this.msg.split('').reverse().join('')
    }
  },
  methods: {
    reversMessage(){
      return this.msg.split('').reverse().join('')
    }
  }
}
</script>

<style scoped>

</style>