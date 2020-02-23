<template>
  <nuxt-link :to="'/posts/' + id">
    <div class="post">
      <p>{{ id }}. {{ title }}</p>
    </div>
  </nuxt-link>
</template>

<script>
export default {
  name: "Post",
  props: ["id", "title"]
};
</script>

<style scoped>
.post {
  padding: 1rem;
  border: 1px solid #2d3436;
  margin: 1rem;
}

.post:hover {
  border: 2px solid #2d3436;
  cursor: pointer;
}

a {
  text-decoration: none;
}

a:hover {
  font-weight: bold;
}
</style>
