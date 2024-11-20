<template>
  <h4>Balance</h4>
  <h1 id="balance" aria-live="polite"> {{ formattedTotal }}</h1>
</template>

<script setup>
import { computed } from 'vue';

// Define the prop with a default value of 0 if not provided
const props = defineProps({
  total: {
    type: Number,
    default: 0,
  },
});

// Compute the formatted total balance
const formattedTotal = computed(() => {
  // Format the number as currency with comma separation for thousands
  return props.total.toLocaleString('en-US', {
    style: 'currency',
    currency: 'KES', // Assuming "KES" is the currency code
  });
});
</script>

<style scoped>
#balance {
  font-weight: bold;
  color: #4caf50; /* A color for emphasis */
}
</style>
