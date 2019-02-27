<template>
  <div class="uk-margin-medium-top">
    <h2 class="uk-heading-bullet uk-margin-medium-bottom">
      {{ brand.name }}
    </h2>
    <DeviceList :devices="brand.devices" />
  </div>
</template>

<script>
import DeviceList from '@/components/device/DeviceList'
export default {
  components: { DeviceList },
  async asyncData({ $axios, params }) {
    const { data: brand } = await $axios.$get(`brand/${params.slug}`)
    return { brand }
  }
}
</script>

<style scoped>
</style>
