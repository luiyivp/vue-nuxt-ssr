<template>
  <div>
    <h1>About Us</h1>
    <p>
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quos iure
      delectus quas harum beatae excepturi tempore deserunt ducimus architecto
      sunt, veniam nesciunt, ipsum voluptas optio maxime a suscipit magni
      laborum!
    </p>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Nuxt SSR | Home",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "A Nuxt.js project sample"
        }
      ],
      htmlAttrs: {
        lang: "en"
      }
    };
  }
};
</script>
