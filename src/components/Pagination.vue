<template>
  <paginate
      :page-count="pages"
      :page-range="3"
      :margin-pages="1"
      :click-handler="changePage"
      :container-class="'pagination'"
      :page-class="'page'"
  >
  </paginate>
</template>

<script>
import Paginate from "vuejs-paginate-next";

export default {
  components: {
    paginate: Paginate,
  },
  props: {
    pages: {
      type: Number,
      required: true
    }
  },
  methods: {
    changePage(e) {
      this.$emit('changePage', Number(e));
    },
  }
}
</script>

<style>

li {
  list-style: none;
}

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
  font-size: 12px;
  line-height: 60px;
  cursor: pointer;
}

.page.active > a{
  color: white;
  font-size: 30px;
}
</style>