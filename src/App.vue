<template>
  <h1>{{ count }}</h1>
</template>

<script>
export default {
  data(){
    return{
      count: 2
    }
  },
  beforeCreate(){//데이터가 정의 되기 전임으로 undefined
    console.log('Before Create!', this.count)
  },
  created(){//html과 연결이 되기 전임으로 null
    console.log('Created!', this.count)
    console.log(document.querySelector('h1'))
  },
  beforeMount(){//html과 연결이 되기 전임으로 null
    console.log('Before Mount!')
    console.log(document.querySelector('h1'))
  },
  mounted(){//화면에 있는 내용을 조회하여 사용하기 위해선 mounted를 사용
    console.log('Mounted!')
    console.log(document.querySelector('h1'))
  }
}
</script>