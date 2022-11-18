<template>
  <div class="home">
    <label>Search Fruit</label>
    <input type="text"  v-model="search" />
    <div v-for="fruit in filterFruits" :key="fruit">
      {{fruit}}
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

import {ref,computed} from 'vue'
export default {
  name: 'HomeView',
  setup(){
    const search =ref('')
    const fruits = ref(["banana","orange","apple", "strawberry", "mongo"])
    const filterFruits =computed(()=>{
      return fruits.value.filter((fruit)=>{
        return fruit.includes(search.value)
      })
    })
    return {search,fruits,filterFruits}
  }
}
</script>
