<template>
  <div>
    <ul>
      <li
        v-for="(todo, index) in tasks"
        @click="deleteTask"
        :key="index"
      >
        {{ index + 1 }}: {{ todo }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ["tasks"],
  methods: {
    deleteTask(index) {
      this.$emit("del-task", index);
    }
  }
};
</script>

<style lang="css" scoped>
li {
  list-style: none;
  font-size: 30px;
  border: 1px dotted grey;
  width: 50%;
  cursor: pointer;
}
</style>
