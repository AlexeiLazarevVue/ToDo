<template>
  <form action="" @submit.prevent>
    <styled-input class="inp" v-bind:value="text" @input="text = $event.target.value" />
    <styled-button class="btn" @click="createItem">Add</styled-button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      text: ''
    }
  }, methods: {
    createItem(event) {
      this.$emit('create', this.text)
      this.text = ''
    }
  }
}
</script>

<style scoped>
  form {
    display: flex;
    justify-content: center;
    margin-bottom: 15px;
    box-shadow: 5px 5px 5px 5px rgba(17, 17, 17, 0.2);
    border-radius: 30px 30px 30px 30px;
  }
  .btn {
    border-radius: 0 30px 30px 0;
    border-left: none;
    box-shadow: none;
  }
  .inp {
    box-shadow: none;
  }
</style>