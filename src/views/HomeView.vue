<script setup lang="ts">
import { useRouter } from 'vue-router';
import TheWelcome from '../components/TheWelcome.vue'
const router = useRouter()
const handleC = ()=>{
  router.push({
    name:'about',
    query:{
      id:'11'
    }
  })
}
</script>

<template>
  <main>
    <TheWelcome />
    <button @click="handleC">about</button>
  </main>
</template>
