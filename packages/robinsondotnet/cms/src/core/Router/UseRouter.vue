<script lang="ts">
import { ref, reactive, onMounted } from 'vue'

export default {
  setup({ Array: routes }) {
    const currentRoute = ref(null)
    const state = reactive({
        currentRoute
    })

    const goTo = (path) => {
      state.currentRoute = routes.find(r => r.path)
    }

    onMounted(() => {
      if (state.currentRoute == null)
        state.currentRoute = routes.find(r => r.default)
    })

    return {
      currentRoute,
      goTo
    }
  },

  render() {
    return this.$scopedSlots.default({
      // NOTE: Pass needed values from router to pages
    })
  }
}
</script>
