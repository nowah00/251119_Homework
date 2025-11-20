<script setup>
import { ref } from 'vue';

const inputRef = ref(null);

const inputValue = ref('');

const onClick = () => {
  inputRef.value.focus();
  alert(inputValue.value);
};
</script>

<template>
  <input ref="inputRef" type="text" v-model="inputValue" />

  <button @click="onClick">click</button>
</template>
