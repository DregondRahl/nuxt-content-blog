<template>
  <div>
    <Header />
    <h1 class="mt-6 text-3xl font-bold md:text-5xl">About</h1>
    <p>
      <nuxt-content :document="about" />
    </p>
  </div>
</template>

<script lang="ts">
export default {
  async asyncData({ $content }: any) {
    const about = await $content('about').fetch()

    return {
      about,
    }
  },
}
</script>
