<template>
  <div class="views">
    <b>{{number}}</b>
    <img class="views__img" src="../assets/eye.png" alt="views">
  </div>
</template>

<script>
export default {
  props: {
    number: {
      type: Number,
      required: true
    }
  }
}
</script>

<style scoped>
.views {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  color: #8D8D8D;
}

.views__img {
  margin-left: 5px;
}
</style>