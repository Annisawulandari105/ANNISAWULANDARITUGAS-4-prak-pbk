<!-- ChildComponent.vue -->
<template>
  <div class="child-component">
    <h2>Child Component</h2>
    <button @click="emitData">Emit Data to Parent</button>
  </div>
</template>

<script>
export default {
  methods: {
    emitData() {
      this.$emit('data-updated', 'Data emitted from Child Component');
    }
  }
}
</script>

<style scoped>
.child-component {
  background-color: #fff;
  padding: 10px;
  margin-bottom: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

button {
  background-color: #007bff;
  color: #fff;
  border: none;
  padding: 5px 10px;
  border-radius: 3px;
  cursor: pointer;
}
</style>