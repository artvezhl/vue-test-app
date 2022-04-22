<template>
  <div class="author">
    <my-link :url="user.links.html">
      <img class="author__photo" :src="user.profile_image.small" alt="author photo">
    </my-link>
    <div class="author__name">
      <my-link :url="user.links.html">
        <b>{{user.name}}</b>
      </my-link>
      <my-link :url="user.links.html">
        <p class="author__login">@{{user.username}}</p>
      </my-link>
    </div>
  </div>
</template>

<script>
export default {
  components: {},

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
  cursor: pointer;
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