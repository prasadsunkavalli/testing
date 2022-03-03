<template>
  <div id="app">
  <h1>Todo Using Class Components</h1>
  <input type="text" placeholder="Add your task...." v-model="value"/>
<button @click="addtask" :disabled="this.value.length==0">Add Task</button>
   <div class="modeling" v-if="this.todoitems.length!==0">
    
    <div  v-for="(todo,index) in this.todoitems" :key="index">
      <div class="datas">
  <input @click="boxclicked" type="checkbox"/>                        
  <p :class="{marked: ischecked}">{{todo}}</p>
  <button>Edit</button>
  <button @click="deletetask(index)">Delete</button>
  </div>
  </div>
  </div>
  </div>  

</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
 

@Component
export default class App extends Vue {
  value = ""
  index = 0
  todoitems:string[] = []
  ischecked= false
  
  

  
addtask(){
  this.todoitems.push(this.value)
  this.value= ""

}

deletetask(index:number){
  this.todoitems.splice(index,1)
}


boxclicked(){
  this.ischecked=!this.ischecked
  
}
}

</script>

<style>

#app{
  text-align: center;
  
}
.datas{
  display: flex;
  justify-content: center;
  align-items: center;
}
.marked{
  text-decoration: line-through;
  
}
</style>
