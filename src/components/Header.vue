<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      @btn-click="$emit('toggleAddTask')"
      :text="showAddTask ? 'Close' : 'Add Task'"
      :color="showAddTask ? 'red' : 'green'"
    />
  </header>
</template>

<script>
import Button from "./Button.vue";

export default {
  name: "Header-comp",
  components: {
    Button,
  },
  props: {
    title: String,
    showAddTask: Boolean,
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
