<template>
  <button><slot></slot></button>
</template>
<script>
export default {
  name: "my-button",
};
</script>
<style scoped>
button {
  margin-top: 20px;
  font-size: 16px;
  padding: 12px 20px;

  background-color: teal;
  color: #fff;
  border: none;
  outline: none;

  cursor: pointer;
}
</style>
