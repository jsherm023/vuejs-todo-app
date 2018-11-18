<template>
  <div class="home">
    <ol>
      <li v-for="task in tasks">task: {{ task.task }} id: {{ task.id }} completed {{ task.completed }}</li>
  </ol>
  <p>task:<input type="text" v-model="newTask.task"></p>
  <p>id:<input type="text" v-model="newTask.id"></p>
  <p>completed:<input type="text" v-model="newTask.completed"></p>

  <p><button v-on:click="addTask()">Click here to add new task</button></p>
  </div>
</template>


<style>
ol {
  padding: 100px;
}
</style>

<script>
export default {
  data: function() {
    return {
      tasks: [
        {task: "Wash your car", id: 1, completed: true},
        {task: "Do the dishes", id: 2, completed: false},
        {task: "Do laundry.", id: 3, completed: false}
      ],
      newTask: {task: "", id: "", completed: ""}
    };
  },
  created: function() {},
  methods: {
    addTask: function() {
      console.log('adding task');
      this.tasks.push(this.newTask);
      this.newTask = {task: "", id: "", completed: ""};
    }

  },
  computed: {}
};
</script>