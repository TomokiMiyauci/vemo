<template>
  <v-icon :color="color" :size="size">{{ icon }}</v-icon>
</template>

<script>
export default {
  props: {
    icon: {
      type: String,
      default: 'fa-check-circle'
    },

    size: {
      type: [String, Number],
      default: undefined
    },

    color: {
      type: String,
      default: 'green'
    }
  }
}
</script>

<style></style>
