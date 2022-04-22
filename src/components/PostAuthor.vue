<template>
  <div class="author">
    <img class="author__photo" :src="user.profile_image.small" alt="author photo">
    <div class="author__name">
      <b>{{user.name}}</b>
      <p class="author__login">@{{user.username}}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    user: {
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
}

@media screen and (min-width: 480px) and (max-width: 767px) {
  .author {
    padding: 10px 0;
  }
}
</style>