<template>
  <div v-for="item in data">
    <post-item :item="item" />
  </div>
</template>

<script>
import PostItem from "@/components/PostItem";

export default {
  components: {PostItem},
  props: {
    data: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
</style>