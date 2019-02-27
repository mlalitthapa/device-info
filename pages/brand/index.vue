<template>
  <div>
    <Brands :brands="brands" />
  </div>
</template>

<script>
import Brands from '@/components/brand/Brands'
export default {
  name: 'Index',
  components: { Brands },
  async asyncData({ $axios }) {
    const { data } = await $axios.$get('brand')
    return { brands: data }
  }
}
</script>

<style scoped>
</style>
