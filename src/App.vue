<template>
  <div class="app">
    <post-list :data="data" />
    <pagination :pages="totalPages" :currentPage="currentPage" @changePage="changePage" />
  </div>
</template>

<script>
import axios from "axios";
import PostList from "@/components/PostList";
import Pagination from "@/components/Pagination";

export default {
  name: 'App',
  components: {PostList, Pagination},
  data() {
    return {
      data: [],
      currentPage: 1,
      limit: 10,
      totalPages: 0
    }
  },
  methods: {
    async fetchData() {
      try {
        const response = await axios.get('https://api.unsplash.com/photos', {
          params: {
            client_id: '_00DLOXkS1ZxO4hzmo1kjwNgn0HCzsm7hdQ4-qrEjtc',
            page: this.currentPage
          }
        });
        // this.totalPages = Math.ceil(response.headers['x-total'] / this.limit);
        this.totalPages = Math.ceil(101 / this.limit);
        console.log('resolve is ', response.data);
        this.data = response.data
      } catch (e) {
        console.log('Error - ', e.message)
      }
    },
    changePage(pageNumber) {
      this.currentPage = pageNumber;
      // this.fetchData();
    }
  },
  mounted() {
    this.fetchData();
  },
  watch: {
    currentPage() {
      this.fetchData();
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto+Condensed:wght@400;700&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Roboto Condensed', sans-serif;
  font-size: 12px;
}

@media screen and (min-width: 480px) {
  .app {
    padding: 0 20px;
  }
}

@media screen and (min-width: 768px) {
  .app {
    padding: 0 54px;
  }
}
</style>
