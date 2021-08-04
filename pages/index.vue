<template>
  <article>
    <h1>{{ page.title }}</h1>
    <nuxt-content :document="page" />
  </article>
</template>

<script lang="ts">
export default {
  async asyncData({ $content }: any ) {
    const page = await $content('hello').fetch()

    return {
      page,
    }
  },
}
</script>
