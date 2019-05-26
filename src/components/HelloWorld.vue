<template>
  <div>
    <button v-bind:title="title">Hover over me</button>

    <button :disabled="isLoading" @click="toggle" :class="{'is-loading':isLoading }">Click me!</button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      isLoading: false,
      title: "Now the title is beign set through javascript"
    };
  },
  methods: {
    toggle() {
      this.isLoading = !this.isLoading;
    }
  }
};
</script>

<style scoped>
.is-loading {
  background: red;
  color: white;
}
</style>
