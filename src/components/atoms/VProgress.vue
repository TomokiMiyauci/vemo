<template>
  <v-icon :color="color" :size="size" class="spin">{{ icon }}</v-icon>
</template>

<script>
export default {
  props: {
    icon: {
      type: String,
      default: 'fa-spinner'
    },

    size: {
      type: [String, Number],
      default: undefined
    },

    color: {
      type: String,
      default: undefined
    }
  }
}
</script>

<style scoped>
@keyframes spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
.spin {
  animation: spin 1.2s linear infinite;
}
</style>
