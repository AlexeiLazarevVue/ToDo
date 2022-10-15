<template>
  <div class="wrapper1">
    {{item.text}}
    <styled-button @click="deleteItem">Delete</styled-button>
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
      isRequired: true
    }
  },
  methods: {
    deleteItem(event) {
      this.$emit('delete', this.item)
    }
  }
}
</script>

<style scoped>
  ul {
    list-style: none;
  }
  div {
    display: flex;
    box-shadow: 5px 5px 5px 5px rgba(17, 17, 17, 0.2);
    background: #ff8a6a;
    padding: 15px;
    margin-bottom: 15px;
    border-radius: 30px;
    justify-content: space-between;
    align-items: center;
  }
</style>