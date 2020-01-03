<template>
  <div>This is the header</div>
  <Router />
  <div> This is the footer</div>
</template>

<script>
import { ref } from 'vue'
import Router from './Router.vue'

export default {
  setup() {
    const foo = ref(0)
    const fetchMethod = () => {
      console.log('fetchMethod called')
    }

    return {
      fetchMethod,
      foo
    }
  }
}
</script>
