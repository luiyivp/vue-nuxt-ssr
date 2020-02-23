<template>
  <div class="post">
    <h2>{{ post.title }}</h2>
    <p>Id: {{ post.id }}</p>
    <p>{{ post.body }}</p>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data: () => ({
    post: {}
  }),
  async created() {
    const res = await axios.get(
      `https://jsonplaceholder.typicode.com/posts/${this.$route.params.id}`
    );
    this.post = res.data;
  }
};
</script>

<style scoped>
.post {
  border: 1px solid whitesmoke;
  padding: 4rem;
}
</style>
