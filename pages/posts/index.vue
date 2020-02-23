<template>
  <div>
    <h1>Posts</h1>
    <Post
      v-for="post in posts"
      :key="post.id"
      :id="post.id"
      :title="post.title"
    />
  </div>
</template>

<script>
import axios from "axios";
import Post from "../../components/Post";

export default {
  components: {
    Post
  },
  data: () => ({
    posts: []
  }),
  async created() {
    try {
      const res = await axios.get(`https://jsonplaceholder.typicode.com/posts`);
      this.posts = res.data;
    } catch (err) {
      console.log(err);
    }
  }
};
</script>
