<template>
  <div class="author">
    <g-image
      alt="Author image"
      class="author__image"
      src="~/assets/images/profile.webp"
      width="180"
      height="180"
      blur="5"
    />

    <h1 v-if="showTitle" class="author__site-title">
      {{ $static.metadata.siteName }}
    </h1>

    <p class="author__intro">Digital practitioner 👨‍💻</p>

    <p class="author__links">
      <a target="_blank" rel="noopener" href="https://twitter.com/micahthobbs"
        >Twitter</a
      >
      <a target="_blank" rel="noopener" href="https://github.com/micahthobbs"
        >GitHub</a
      >
      <a
        target="_blank"
        rel="noopener"
        href="https://www.linkedin.com/in/micahthobbs"
        >LinkedIn</a
      >
    </p>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
  props: ["showTitle"],
};
</script>

<style lang="scss">
.author {
  margin: 0 auto;
  max-width: 500px;
  text-align: center;
  padding: calc(var(--space) / 2) 0;

  &__image {
    border-radius: 10%;
    width: 100px;
    height: 100px;
    margin-bottom: 1em;
  }

  &__intro {
    opacity: 0.8;
  }

  &__site-title {
    font-size: 1.5em;
  }

  &__links {
    margin-top: -0.5em;
    a {
      margin: 0 0.5em;
    }
  }
}
</style>
