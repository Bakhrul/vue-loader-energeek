<script setup lang="ts">
  const props = defineProps({
    color: {
      type: String,
      required: false,
      default: '#EE7B33'
    }
  });
</script>

<template>
  <div>
    <div class="vue-loader-energeek" :style="`border: 5px solid ${props.color};`"></div>
  </div>
</template>