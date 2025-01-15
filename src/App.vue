<script>
export default {
  data() {
    return {
      name: "John Doe",
      status: "pending",
      tasks: ["Task One", "Task Two", "Task Three"],
      link: "https://google.com",
    };
  },
};
</script>

<template>
  <h1>{{ name }}</h1>
  <p v-if="status === 'active'">User is Active</p>
  <p v-else-if="status === 'pending'">User is Pending</p>
  <p v-else>User is inactive</p>

  <h3>Tasks:</h3>
  <ul>
    <li v-for="task in tasks" :key="task">
      {{ task }}
    </li>
  </ul>
  <a v-bind:href="link">click me for google</a>
</template>

<style scoped>
h1 {
  color: red;
}
</style>
