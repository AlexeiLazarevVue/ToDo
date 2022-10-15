<template>
  <button>
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: 'styled-button'
}
</script>

<style scoped>
button {
    box-shadow: 5px 5px 5px 5px rgba(17, 17, 17, 0.2);
    background: #ff8a6a;
    padding: 15px;
    border-radius: 30px;
    border: 1px solid #1d1d1d;
}
</style>