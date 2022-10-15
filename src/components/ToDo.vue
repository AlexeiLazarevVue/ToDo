<template>
<div class="todo-wrapper">
  <to-do-form @create="createItem"></to-do-form>
  <to-do-item @delete="deleteItem" v-for="toDoComponent in toDoComponents" :item="toDoComponent" :key="toDoComponent.id" class="to-do-item">
  </to-do-item>
</div>
</template>

<script>
import ToDoForm from '@/components/ToDoForm.vue'
import ToDoItem from '@/components/ToDoItem.vue'
export default {
  components: { ToDoItem, ToDoForm },
  data() {
    return {
      toDoComponents: [],
        limit: 11
    }
  }, methods: {
    createItem(item) {
      if(this.toDoComponents.length <= this.limit) {
        this.toDoComponents.push({id: Date.now(), text: item})
      }
    },
    deleteItem(item) {
      this.toDoComponents = this.toDoComponents.filter(arrayItem => arrayItem.id != item.id)
    }
  }
}
</script>

<style scoped>
  .todo-wrapper {
    min-height: 500px;
    width: 300px;
    box-shadow: 5px 5px 5px 5px rgba(17, 17, 17, 0.2);
    background: #ff7f5b;
    margin: 20px;
    border-radius: 30px;
    padding: 15px;
  }
</style>