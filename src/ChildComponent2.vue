<!-- ChildComponent2.vue -->
<template>
    <div class="child-component2">
      <h2>Child Component 2</h2>
      <p>Data from Parent Component: {{ data }}</p>
    </div>
  </template>
  
  <script>
  export default {
    props: ['data'],
    mounted() {
      console.log('Data from Parent Component:', this.data);
    }
  }
  </script>
  
  <style scoped>
  .child-component2 {
    background-color: #fff;
    padding: 10px;
    margin-bottom: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
  }
  
  p {
    color: #333;
  }
  </style>