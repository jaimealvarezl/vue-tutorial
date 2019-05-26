<template>
  <div>
    <h2>All Tasks</h2>
    <ul>
      <li v-for="task in tasks" v-text="task.description"></li>
    </ul>

    <h2>Incompleted Tasks</h2>
    <ul>
      <li v-for="task in incompleteTasks" v-text="task.description"></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      tasks: [
        { description: "Go to store", completed: true },
        { description: "Finish screen cast", completed: false },
        { description: "Make donation", completed: false },
        { description: "Clear inbox", completed: false },
        { description: "Make dinner", completed: false },
        { description: "Clear room", completed: true }
      ]
    };
  },
  computed: {
    incompleteTasks() {
      return this.tasks.filter(task => !task.completed);
    }
  }
};
</script>

<style scoped>
</style>
