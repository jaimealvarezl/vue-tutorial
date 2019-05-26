<template>
  <div>
    <ul>
      <li v-for="name in names" v-text="name"></li>
    </ul>

    <input type="text" v-model="newName">
    <button @click="addName">Add Name</button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data() {
    return { names: ["joe", "mary", "jane", "jack"], newName: "Mary" };
  },
  methods: {
    addName() {
      this.names.push(this.newName);
      this.newName = "";
    }
  },
  mounted() {
    console.log("Mounted");
  }
};
</script>

<style scoped>
</style>
