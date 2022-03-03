<template>
  <div id="app">
    <h>conter app using vuex</h>
    <h3>{{$store.state.count}}</h3>
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';


export default Vue.extend({
  name: 'App',
  components: {},
  methods:{
    increment() {
    this.$store.commit('increment')
    
  },
     decrement() {
    this.$store.commit('decrement')
    

  }
  }
});
</script>

<style>
#app{
  text-align: center;
}

</style>
