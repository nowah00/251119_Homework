<script setup>
import { ref, computed } from 'vue';

const searchText = ref('');

const warningMessage = computed(() => {
  if (searchText.value.length > 10) {
    return '10자를 초과했습니다!';
  }
});
</script>

<template>
  <input type="text" v-model="searchText" />
  <p style="color: red">{{ warningMessage }}</p>
</template>
