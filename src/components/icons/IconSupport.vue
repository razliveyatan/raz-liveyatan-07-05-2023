<script setup lang="ts">
type iconProps = {
    selected: boolean;
}
defineProps<iconProps>()

</script>

<template>
  <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" :class="{ selected: selected }" fill="white">
    <path
      d="M10 3.22l-.61-.6a5.5 5.5 0 0 0-7.666.105 5.5 5.5 0 0 0-.114 7.665L10 18.78l8.39-8.4a5.5 5.5 0 0 0-.114-7.665 5.5 5.5 0 0 0-7.666-.105l-.61.61z"
    />
  </svg>
</template>

<style scoped>
.selected {
  fill: #f31919;
}
</style>
