<template>
  <div>
    <post-list :data="mockData" />
  </div>
</template>

<script>
import PostList from "@/components/PostList";

export default {
  name: 'App',
  components: {PostList},
  data() {
    return {
      mockData: [
        {id: 1, image_name: 'image name', image_url: 'https://upload.wikimedia.org/wikipedia/commons/6/62/Starsinthesky.jpg', author_photo: 'https://eitrawmaterials.eu/wp-content/uploads/2016/09/person-icon.png', author_name: '\n' +
              'Jason Mowry', author_login: 'jason_mowry_photo', views: 43000},
        {id: 2, image_name: 'image name', image_url: 'https://upload.wikimedia.org/wikipedia/commons/6/62/Starsinthesky.jpg', author_photo: 'https://eitrawmaterials.eu/wp-content/uploads/2016/09/person-icon.png', author_name: '\n' +
              'Jason Mowry', author_login: 'jason_mowry_photo', views: 43000},
        {id: 3, image_name: 'image name', image_url: 'https://upload.wikimedia.org/wikipedia/commons/6/62/Starsinthesky.jpg', author_photo: 'https://eitrawmaterials.eu/wp-content/uploads/2016/09/person-icon.png', author_name: '\n' +
              'Jason Mowry', author_login: 'jason_mowry_photo', views: 43000},
        {id: 4, image_name: 'image name', image_url: 'https://upload.wikimedia.org/wikipedia/commons/6/62/Starsinthesky.jpg', author_photo: 'https://eitrawmaterials.eu/wp-content/uploads/2016/09/person-icon.png', author_name: '\n' +
              'Jason Mowry', author_login: 'jason_mowry_photo', views: 43000},
        {id: 5, image_name: 'image name', image_url: 'https://upload.wikimedia.org/wikipedia/commons/6/62/Starsinthesky.jpg', author_photo: 'https://eitrawmaterials.eu/wp-content/uploads/2016/09/person-icon.png', author_name: '\n' +
              'Jason Mowry', author_login: 'jason_mowry_photo', views: 43000},
        {id: 6, image_name: 'image name', image_url: 'https://upload.wikimedia.org/wikipedia/commons/6/62/Starsinthesky.jpg', author_photo: 'https://eitrawmaterials.eu/wp-content/uploads/2016/09/person-icon.png', author_name: '\n' +
              'Jason Mowry', author_login: 'jason_mowry_photo', views: 43000},
        {id: 7, image_name: 'image name', image_url: 'https://upload.wikimedia.org/wikipedia/commons/6/62/Starsinthesky.jpg', author_photo: 'https://eitrawmaterials.eu/wp-content/uploads/2016/09/person-icon.png', author_name: '\n' +
              'Jason Mowry', author_login: 'jason_mowry_photo', views: 43000},
        {id: 8, image_name: 'image name', image_url: 'https://upload.wikimedia.org/wikipedia/commons/6/62/Starsinthesky.jpg', author_photo: 'https://eitrawmaterials.eu/wp-content/uploads/2016/09/person-icon.png', author_name: '\n' +
              'Jason Mowry', author_login: 'jason_mowry_photo', views: 43000},
      ]
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
</style>
