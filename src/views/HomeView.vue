<template>
  <div class="home">
    <p ref='p' >My name is {{name}} .Iam {{age}}</p>
    <button @click="addAge">show hello</button>
  </div>
</template>

<script>
// @ is an alias to /src

import {ref} from 'vue'
export default {
  name: 'HomeView',
  setup(){
    let name ="abde"
    let age =37
    const p = ref(null)
    const addAge =()=>{
      console.log(p,p.value)
      p.value.classList.add('test')
      p.value.textContent="hello joker"
    }
    return{name,age,addAge,p}
  }
}
</script>
