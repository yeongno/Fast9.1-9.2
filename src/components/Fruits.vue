<template>
  <section v-if="hasFruit">
    <h1>Fruits</h1>
    <ul>
      <li
      v-for="fruit in fruits"
      :key="fruit">
      {{fruit}}
      </li>
    </ul>
  </section>
  <section>
    <h1>Reverse Fruits</h1>
    <ul>
      <li v-for="fruit in reverseFruits" :key="fruit">{{ fruit }}</li>
    </ul>
  </section>
</template>

<script>
export default {
  data(){
    return{
      fruits: [
        'Apple', 'Banana', 'Cherry'
      ]
    }
  },
  computed:{
    hasFruit(){
      return this.fruits.length > 0
    },
    reverseFruits(){
      return this.fruits.map(fruit => {
        return fruit.split('').reverse().join('')
        //해당하는 배열의 문자열을 각 배열에 넣고 뒤집은 다음 하나의 문자열로 만들어 줌
      })
    }
  }
}
</script>

<style scoped>

</style>