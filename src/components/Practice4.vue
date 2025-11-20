<script setup>
import { computed, reactive } from 'vue';

const cart = reactive({
  item1: {
    price: 10000,
    count: 1,
  },

  item2: {
    price: 5000,
    count: 1,
  },
});
const totalPrice = computed(() => {
  return (
    cart.item1.price * cart.item1.count + cart.item2.price * cart.item2.count
  );
});
</script>

<template>
  <p>item1 price: {{ cart.item1.price }}</p>
  <p>item1 count: {{ cart.item1.count }}</p>
  <br />
  <p>item2 price: {{ cart.item2.price }}</p>
  <p>item2 count: {{ cart.item2.count }}</p>
  <br />
  <h3>Total Price: {{ totalPrice }}</h3>
</template>
