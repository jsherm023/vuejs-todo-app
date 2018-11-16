<template>
  <div class="home">
    <ol>
      <h1>{{ message }}</h1>
      <li>{{ task1 }}</li>
      <li>{{ task2 }}</li>
      <li> {{ task3 }} </li>
  </ol>
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
      message: "Complete the following tasks!",
      task1: "Wash your car",
      task2: "Do the dishes",
      task3: "Do laundry."
    };
  },
  created: function() {},
  methods: {},
  computed: {}
};
</script>