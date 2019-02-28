<template>
  <div class="uk-margin-medium-top">
    <Search :searched="searchQuery" />
    <h2 class="uk-heading-divider">
      Search results for <strong>{{ searchQuery }}</strong>
    </h2>
    <DeviceList :devices="devices" />
  </div>
</template>

<script>
import Search from '@/components/Search'
import DeviceList from '@/components/device/DeviceList'

export default {
  watchQuery: ['query'],
  key: to => to.fullPath,
  components: { DeviceList, Search },
  validate({ query: { query: searchQuery } }) {
    return searchQuery.trim()
  },
  async asyncData({ query, $axios }) {
    const { query: searchQuery } = query
    const { data: devices } = await $axios.$get(`search?query=${searchQuery}`)
    return { searchQuery, devices }
  }
}
</script>

<style scoped>
</style>
