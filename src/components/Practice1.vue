<script setup>
import { ref, computed, watch } from 'vue';
// ref 값을 이용할 때는 .value 꼭 붙이기!
const count = ref(0);

// computed return 꼭 해주기!
const doubledCount = computed(() => {
  console.log(count.value);
  return count.value * 2;
});

// methods는 함수로 씀. 별도에 methods(() => {})안해도됌.
const increment = () => {
  console.log(count.value);
  count.value++;
};

const updateCount = watch(count, (newVal, oldVal) => {
  console.log(`Count changed from ${oldVal} to ${newVal}`);
});
</script>

<template>
  <div>
    <p>Count: {{ count }}</p>
    <p>Doubled Count: {{ doubledCount }}</p>
    <button @click="increment">Increment</button>
  </div>
</template>
