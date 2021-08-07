<template>
<div>
  <Header />
  <h1>About</h1>
</div>
</template>

<script lang="ts">
export default {
  async asyncData({ $content }: any) {
    const articles = await $content('about').fetch()

    return {
      articles,
    }
  },
}
</script>
