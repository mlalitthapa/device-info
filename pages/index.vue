<template>
  <div>
    <div class="uk-flex uk-flex-center">
      <div class="uk-width-2-3 uk-margin-medium-top">
        <Search />
      </div>
    </div>
    <div>
      <h2 class="uk-heading-divider">
        Latest Devices
      </h2>
      <DeviceList :devices="devices" />
    </div>
  </div>
</template>

<script>
import Search from '@/components/Search'
import DeviceList from '@/components/device/DeviceList'

export default {
  components: { DeviceList, Search },
  async asyncData({ $axios }) {
    const { data } = await $axios.$get('latest')
    return { devices: data }
  }
}
</script>
