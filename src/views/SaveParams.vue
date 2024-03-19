<script setup lang="ts">
import { onMounted } from 'vue';
import { useRoute, useRouter } from 'vue-router';
const router = useRouter()
const route = useRoute()

const handleC = ()=>{
  router.push({
    name:'about',
    query:{
      id:'11'
    }
  })
}
onMounted(()=>{
  console.log('数据变化')
  // console.log('history.state', history.state)
  console.log('this.params', route.params)
})
</script>

<template>
  <main>
    <button @click="handleC">about</button>
  </main>
</template>
