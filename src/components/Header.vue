<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      :text="showAddTask ? 'Close' : 'Add Data'"
      @click="showAddForm"
      :color="showAddTask ? 'Red' : 'Green'"
    ></Button>
    <!-- <Button text="Update" color="blue"></Button>
    <Button text="Delete" color="red"></Button> -->
  </header>
</template>
<script>
import Button from "./Button";
export default {
  name: "Header",
  props: {
    title: String,
    showAddTask: Boolean
  },
  components: { Button },
  methods: {
    showAddForm() {
      this.$emit("show-add");
    }
  },
  emits: ["show-add"]
};
</script>
<style scoped>
header {
  display: flex;
  justify-content: space-around;
  align-content: center;
  margin-bottom: 20px;
}
</style>
