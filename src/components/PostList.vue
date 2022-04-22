<template>
  <div class="posts">
    <post-item v-for="item in data" :key="item.id" :item="item" />
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
@media screen and (min-width: 768px) {
  .posts {
    width: 680px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    column-gap: 20px;
    margin: 0 auto;
  }
}
</style>