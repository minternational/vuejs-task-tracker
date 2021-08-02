<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      @btn-click="$emit('show-form')"
      v-bind:text="showAddTask ? 'Cancel' : 'Add Task'"
      v-bind:color="showAddTask ? 'Red' : 'Green'"
    />
  </header>
</template>

<script>
import Button from "./Button.vue";

export default {
  name: "Header",
  props: {
    title: String,
    showAddTask: Boolean,
  },
  components: {
    Button,
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
