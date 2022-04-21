<template>
  <div class="author">
    <img class="author__photo" :src="post.author_photo" alt="author photo">
    <div class="author__name">
      <b>{{post.author_name}}</b>
      <p class="author__login">@{{post.author_login}}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.author {
  display: flex;
  flex-direction: row;
  padding: 10px;
}

.author__photo {
  width: 30px;
  height: 30px;
  border-radius: 50%;
}

.author__name {
  margin-left: 10px;
}

.author__login {
  color: #8D8D8D;
;
}
</style>