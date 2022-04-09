<template>
<input 
type="text"
@keydown.ctrl.shift.a="handler">
</template>

<script>
export default {
  methods:{
    handler(event){
      console.log('Enter!!')
    }  
  }
}
</script>

