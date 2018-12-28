<template>
  <button :class="state">{{ title }}</button>
</template>

<script>
export default {
  name: "MyButton",
  props: {
    title: String,
    state: String
  }
};
</script>

<style scoped>

button {
  width: 100%;
  padding: 6px;
  border-radius: 2px;
  cursor: pointer;
}

.outline{
  background-color: white;
  color: green;
  border: 1px solid green;
}

.block{
  background-color: green;
  color: white;
  border: 1px solid green;
}

</style>
