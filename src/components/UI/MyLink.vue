<template>
  <a :href="url" class="link" target="_blank">
    <slot></slot>
  </a>
</template>

<script>
export default {
  name: 'my-link',
  props: {
    url: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
.link {
  color: inherit;
  text-decoration: none;
}
</style>