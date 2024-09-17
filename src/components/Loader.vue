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
    <div class="loader-component" :style="`border: 5px solid ${props.color};`"></div>
  </div>
</template>

<style scoped>
  .loader-component {
    border-radius: 50%;
    border-top: 5px solid #f2f2f2 !important;
    width: 40px;
    height: 40px;
    -webkit-animation: spin 2s linear infinite;

    animation: spin 2s linear infinite;
  }

  /* Safari */
  @-webkit-keyframes spin {
    0% {
      -webkit-transform: rotate(0deg);
    }

    100% {
      -webkit-transform: rotate(360deg);
    }
  }

  @keyframes spin {
    0% {
      transform: rotate(0deg);
    }

    100% {
      transform: rotate(360deg);
    }
  }
</style>