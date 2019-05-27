<template>
  <div>
    <ul>
      <Task>Go to store</Task>
      <Task>Go to bank</Task>
      <Task>Go to work</Task>
    </ul>
  </div>
</template>

<script>
import Task from "./Task";
export default {
  name: "HelloWorld",
  components: { Task }
};
</script>

<style scoped>
</style>
