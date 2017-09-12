<template>

  <div class="postslist">
    <div class="container">
      <h1>Listagem de Posts</h1>
      <ul>
        <li v-for="post in posts">{{post.title}}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'postslist',
  data () {
    return {
      posts: []
    }
  },

  created: function () {
    this.$http.get('http://jsonplaceholder.typicode.com/posts')
      .then(response => {
        console.log(response);
        this.posts = response.data;
      });
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .media-object {
    width: 128px;
    padding: 10px;
  }
  .media {
    border-top: 1px solid lightgray;
    padding-top: 20px;
  }
</style>
