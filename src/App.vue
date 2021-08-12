<template>
<div class="container">
  <h1>{{ title }}</h1>
  <TaskForm />
  <TaskList />
</div>
</template>

<script>
import TaskForm from './components/TaskForm.vue';
import TaskList from './components/TaskList.vue';

export default {
  name: 'App',
  components: {
    TaskForm,
    TaskList
  },
  methods: {
    saySomething() {
      console.log("Hello There!!!")
    }
  },
  data() {
    return {
      title: "Task Manager"
    }
  }
}
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
  border: 1px solid lightgrey;
  width: 500px;
  margin: 0 auto;
  border-radius: 10px;
}
</style>
