<template>
  <div>
    <p>{{ message }}</p>
    <button @click="increment">Count: {{ count }}</button>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const count = ref(0);
    const message = "Hello from Vue!";

    const increment = () => {
      count.value++;
    };

    return {
      count,
      message,
      increment,
    };
  },
};
</script>

<style scoped>
button {
  margin-top: 10px;
  padding: 8px 12px;
  font-size: 16px;
  border: none;
  cursor: pointer;
}
</style>
