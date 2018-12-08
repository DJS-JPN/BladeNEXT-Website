<template>
  <h1>{{ data }}</h1>
</template>


<script>
export default {
  data() {
    return {
      data: ''
    }
  },
  async asyncData({ app }) {
    const response = await app.$axios.$get(
      'https://blade-next.now.sh/api/application'
    )
    return { data: response }
  }
}
</script>
