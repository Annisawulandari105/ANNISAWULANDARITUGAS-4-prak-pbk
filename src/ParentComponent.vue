<!-- ParentComponent.vue -->
<template>
  <div class="container">
    <h1>Parent Component</h1>
    <ChildComponent @data-updated="handleDataUpdated" />
    <ChildComponent2 :data="childData" />
    <SlotComponent>
      <h2>Slot Content 1</h2>
      <p>This is the content of Slot 1</p>
    </SlotComponent>
    <SlotComponent>
      <h2>Slot Content 2</h2>
      <p>This is the content of Slot 2</p>
    </SlotComponent>
  </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue';
import ChildComponent2 from './ChildComponent2.vue';
import SlotComponent from './SlotComponent.vue';

export default {
  components: {
    ChildComponent,
    ChildComponent2,
    SlotComponent
  },
  data() {
    return {
      childData: ''
    };
  },
  methods: {
    handleDataUpdated(data) {
      this.childData = data;
    }
  }
}
</script>

<style scoped>
.container {
  background-color: #f2f2f2;
  padding: 20px;
  border-radius: 5px;
}

h1 {
  color: #333;
}

h2 {
  margin-top: 20px;
  color: #666;
}

p {
  color: #999;
}
</style>