<template>
  <div class="app">
    <post-list :data="data" />
  </div>
</template>

<script>
import axios from "axios";
import PostList from "@/components/PostList";

export default {
  name: 'App',
  components: {PostList},
  data() {
    return {
      data: []
    }
  },
  methods: {
    async fetchData() {
      try {
        const resolve = await axios.get('https://api.unsplash.com/photos/?client_id=_00DLOXkS1ZxO4hzmo1kjwNgn0HCzsm7hdQ4-qrEjtc');
        console.log('resolve is ', resolve.data);
        this.data = resolve.data
      } catch (e) {
        console.log('Error - ', e.message)
      }
    },
  },
  mounted() {
    this.fetchData();
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
