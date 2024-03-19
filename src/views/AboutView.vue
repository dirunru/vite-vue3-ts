<template>
  <div class="about">
    <div class="relative_div">
      <div class="box"></div>
    </div>
    <div class="relative_div1">
      <div class="box"></div>
    </div>
    <div class="relative_div1">
      <div class="box"></div>
    </div>
    <button @click="handleC">去saveParams页面</button>
  </div>
</template>
<script setup lang="ts">
import { useRouter } from 'vue-router';

const router = useRouter()
let id:number = 111
const handleC = () =>{
  router.push({
    name:'saveParams',
    // state: {
    //   id
    // }
    params:{
      id
    }
  })
}
</script>
<style lang="less" scoped>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    // display: flex;
    // align-items: center;
  }
}
.about {
  border:solid 1px red;
  position: relative;
  .relative_div {
    position: absolute;
    border: solid 1px seagreen; 
    left: 100px;
    top:100px;
    width: 100px;
    height: 100px;
  }
  .relative_div1 {
    display: inline-block;
    border: solid 1px orange; 
    width: 200px;
    height: 200px;
  }
}
</style>
