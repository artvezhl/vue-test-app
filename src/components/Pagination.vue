<template>
  <div class="pagination">
    <div
        class="page"
        :class="{
          'page_current': page === currentPage
        }"
        v-for="page in pages"
        :key="page"
        @click="changePage"
    >{{ page }}</div>
  </div>
</template>

<script>
export default {
  props: {
    pages: {
      type: Number,
      required: true
    },
    currentPage: {
      type: Number,
      required: true
    }
  },
  methods: {
    changePage(e) {
      // console.log()
      this.$emit('changePage', Number(e.target.innerHTML));
    }
  }
}
</script>

<style scoped>
.pagination {
  position: fixed;
  bottom: 0;
  left: 0;
  height: 60px;
  width: 100%;
  background: rgba(0,0,0,.9);
  display: flex;
  justify-content: center;
  align-items: center;
}

.page {
  color: #8D8D8D;
  padding: 4px;
  font-size: 14px;
  line-height: 60px;
  cursor: pointer;
}

.page_current {
  color: white;
  font-size: 20px;
}
</style>