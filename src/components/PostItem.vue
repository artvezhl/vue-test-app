<template>
  <div class="post" :key="item.id">
    <post-author :post="item"/>
    <img class="post__img" :src="item.image_url" :alt="item.image_name">
    <views-number :number="item.views" />
  </div>
</template>

<script>
import PostAuthor from "@/components/PostAuthor";
import ViewsNumber from "@/components/ViewsNumber";

export default {
  components: {PostAuthor, ViewsNumber},
  props: {
    item: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.post {
  margin-bottom: 10px;
}
.post__img {
  object-fit: cover;
  width: 100%;
  max-height: 230px;
  margin-bottom: 10px;
}
</style>