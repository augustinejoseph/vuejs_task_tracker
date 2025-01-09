<template>
  <div class="container">
    <Header title="Header Props..." />
    <Tasks :tasks="tasks" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Header from './components/Header.vue';
import Tasks from './components/Tasks.vue';
export default defineComponent({
  name: 'App',
  components: {
    Header, Tasks
  },
  data() {
    return {
      tasks: [
        // { id: 1, name: 'Doctors Appointment' },
        // { id: 2, name: 'Teachers Appointment' }
      ]
    }
  },
  created() {
    this.tasks = [
      { id: 1, name: 'Doctors Appointment', reminder : true },
      { id: 2, name: 'Teachers Appointment', reminder : false }
    ]
  }
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px solid steelblue;
  padding: 30px;
  border-radius: 5px;
}

.btn {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}
</style>
