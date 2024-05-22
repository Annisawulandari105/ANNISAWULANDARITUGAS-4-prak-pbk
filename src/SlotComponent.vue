<!-- SlotComponent.vue -->
<template>
    <div class="slot-component">
      <h2>Slot Component</h2>
      <slot></slot>
    </div>
  </template>
  
  <script>
  export default {}
  </script>
  
  <style scoped>
  .slot-component {
    background-color: #fff;
    padding: 10px;
    margin-bottom: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
  }
  
  h2 {
    color: #333;
  }
  </style>