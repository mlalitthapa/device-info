<template>
  <div>
    <div class="uk-flex uk-flex-center">
      <div class="uk-width-2-3 uk-margin-medium-top">
        <Search />
      </div>
    </div>
    <Latest :devices="devices" />
  </div>
</template>

<script>
import Search from '@/components/Search'
import Latest from '@/components/device/Latest'

export default {
  components: { Latest, Search },
  async asyncData({ $axios }) {
    const { data } = await $axios.$get('latest')
    return { devices: data }
  }
}
</script>
