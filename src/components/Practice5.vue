<script setup>
import { ref } from 'vue';

const inputRef = ref(null);

const onClick = () => {
  // 클릭시 inputRef로 포커스
  inputRef.value.focus();

  // inputRef의 value를 Alert로 출력
  alert(inputRef.value.value);
};
</script>

<template>
  <input ref="inputRef" type="text" @keyup.enter="onClick" />
  <button @click="onClick">click</button>
</template>
