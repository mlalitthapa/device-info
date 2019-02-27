<template>
  <div class="uk-margin-small-top">
    <Device :device="device" />
  </div>
</template>

<script>
import Device from '@/components/device/Device'
export default {
  components: { Device },
  async asyncData({ params, $axios }) {
    const { data: device } = await $axios.$get(`device/${params.slug}`)
    return { device }
  }
}
</script>

<style scoped>
</style>
