<template>
  <div class="author">
    <g-image
      alt="Image de Quentin Durantay"
      class="author__image"
      src="~/assets/images/quentin.jpg"
      width="180"
      height="180"
      blur="5"
    />

    <h1 v-if="showTitle" class="author__site-title">{{ $static.metadata.siteName }}</h1>

    <p class="author__intro">
      Former Growth Engineer & Product Manager at
      <a href="//www.dolead.com/" target="_blank">Dolead</a>
      <br />Co-founder & CTO/CPO at
      <a href="//www.chasseurparticulier.com/" target="_blank">Chasseur Particuliers</a>
      <br />Founder at
      <a href="//www.codingformarketers.io/" target="_blank">Coding for Marketers</a>
    </p>

    <p class="author__links">
      <a href="//twitter.com/quentindty" target="_blank">Follow on Twitter</a>
      <a href="//linkedin.com/in/qdurantay" target="_blank">LinkedIn</a>
      <a href="//github.com/vonstruddle" target="_blank">GitHub</a>
      <a href="mailto:quentin.durantay@gmail.com" target="_blank">Email</a>
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
  props: ['showTitle']
}
</script>

<style lang="scss">
.author {
  margin: 0 auto;
  max-width: 500px;
  text-align: center;
  padding: calc(var(--space) / 2) 0;

  &__image {
    border-radius: 100%;
    width: 90px;
    height: 90px;
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
