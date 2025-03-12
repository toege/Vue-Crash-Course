<script>
export default {
  data() {
    return {
      name: "Jonas Donas",
      status: "pending",
      tasks: ['task 1', 'task 2', 'task 3'],
      link: 'https://google.com',
    };
  },
  methods: {
    toggleStatus() {
      if (this.status === 'active') {
        this.status = 'pending';
      }
      else if (this.status === 'pending') {
        this.status = 'inactive';
      }
      else {
        this.status = 'active';
      }
    }
  },
}
</script>

<template>
  <h1>{{ name }}</h1>
  <p v-if="status === 'active'">User is active</p>
  <p v-else-if="status === 'pending'">User is pending</p>
  <p v-else>User is inactive</p>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>
  <br/>
  <!-- <a v-bind:href="link">Clik for Google</a> -->
  <a :href="link">Google</a>
  <br/>
  <button v-on:click="toggleStatus">Change Status</button>
  <br/>
</template>