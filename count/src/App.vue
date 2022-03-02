<template>
  <div id="app">
   <h1>{{counter}}</h1>
   <button class="bty" :disabled="counter<=0" @click="decrement">-</button>
   <button class="bty" @click="increment">+</button>
   <p v-if="counter==0">Value equal to zero so - button disabled</p>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';


@Component
export default class App extends Vue {
  counter = 0
decrement(){
  this.counter-= 1
}
increment(){
  this.counter+=1
}

}
</script>

<style>
#app{
  text-align: center;
}
.bty{
  margin-left: 10px;
}
</style>
