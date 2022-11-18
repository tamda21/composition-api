<template>
  <div class="home">
    <p  >My name is {{name}} .Iam {{age}}</p>
    <input type="text"  v-model="name" />
    <button @click="updateValue">Update</button>
  </div>
</template>

<script>
// @ is an alias to /src

import {ref} from 'vue'
export default {
  name: 'HomeView',
  setup(){
    const name =ref("abde")
    const age =ref(37)
    const updateValue =()=>{
    name.value="loujaine"
    age.value=1
    }
    return{name,age,updateValue,age,name}
  }
}
</script>
