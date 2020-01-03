<template>
  <h1>Not Found Page {{ notFoundUrl }}</h1>
</template>

<script>
export default {
  setup({ url }) {
    return {
      notFoundUrl: url
    }
  }
}
</script>
