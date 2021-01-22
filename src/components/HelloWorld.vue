<template>
  <div>
    ceshi
  </div>
</template>

<script>
import { computed, onUnmounted } from 'vue'
import { useStore } from 'vuex'
export default {
  setup () {
    const store = useStore()
    const testData = computed(() => store.getters.testData)
    // console.log('testData', testData)
    onUnmounted(() => {
      console.log('testData', testData)
    })
    return {
      testData
    }
  }
}
</script>

<style lang="scss" scoped>

</style>
