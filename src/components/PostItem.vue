<template>
  <div class="post">
    <post-author :user="item.user"/>
    <img class="post__img" :src="item.urls.regular" alt="user image">
    <views-number :number="item.likes" />
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
  height: 230px;
  margin-bottom: 10px;
}

@media screen and (min-width: 480px) and (max-width: 767px) {
  .post__img {
    max-height: 300px;
  }
}

@media screen and (min-width: 768px) {
  .post__img {
    /*width: 320px;*/
    max-height: 230px;
  }

  .post {
    width: 320px;
  }
}
</style>