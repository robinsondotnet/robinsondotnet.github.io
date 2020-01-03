<template>
  <UseRouter :routes="routes" />
</template>
<script>
import CMS from './pages/CMS.vue'
import NotFound from './pages/NotFound.vue'
import useRouter from './core/Router/UseRouter.vue'

const routes = [
  { name: 'CMS', default: true, component: CMS },
  { name: '404', component: NotFound }
]

export default {
  setup() {
    return {
      routes
    }
  }
}
</script>
