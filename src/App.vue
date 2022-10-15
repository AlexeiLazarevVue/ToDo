<template>
  <div class="wrapper">
    <to-do class="todo"></to-do>
    <to-do class="done"></to-do>
    <to-do class=""></to-do>
  </div>
</template>

<script>
import ToDo from '@/components/ToDo.vue'
export default {
  components: { ToDo },
  
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.wrapper {
  display: flex;
  height: 100vh;
  align-items: center;
  justify-content: center;
  font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
  background: #fe724b;
}
</style>
