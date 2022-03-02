<template>
  <div class="cent">
    <h1>{{count}}</h1>
<button class="but" @click="sub">-</button>
<button class="but" @click="addi">+</button>
  </div>
</template>

<script>
  export default {
    count :0
  }
</script>

<style scoped>
.cent{
  text-align: center;
}
.but{
  margin-left: 50px;
}
</style>