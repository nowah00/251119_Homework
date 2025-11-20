<script setup>
import { ref } from 'vue';

const inputRef = ref(null);

const onClick = () => {
  inputRef.value.focus();

  alert(inputRef.value.value);
};
</script>

<template>
  <input ref="inputRef" type="text" />
  <button @click="onClick">click</button>
</template>
