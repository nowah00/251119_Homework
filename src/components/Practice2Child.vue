<script setup>
// props 정의
const props = defineProps({
  name: String,
});

// emit 정의
const emit = defineEmits(['greet']);

// 메서드
const sendGreeting = () => {
  emit('greet', `Hello, ${props.name}!`);
};
</script>

<template>
  <div>
    <button @click="sendGreeting">Send Greeting</button>
  </div>
</template>
