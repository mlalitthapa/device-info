<template>
  <div class="uk-margin-medium-top">
    <h2 class="uk-heading-bullet uk-margin-medium-bottom">
      {{ brand.name }}
    </h2>
    <DeviceList :devices="brand.devices" />
    <div class="uk-margin-medium-top">
      <no-ssr>
        <Paginate v-if="brand.pages" :pages="brand.pages" />
      </no-ssr>
    </div>
  </div>
</template>

<script>
import DeviceList from '@/components/device/DeviceList'
import Paginate from '@/components/device/Paginate'

export default {
  components: { Paginate, DeviceList },
  async asyncData({ $axios, params }) {
    const { data: brand } = await $axios.$get(`brand/${params.slug}`)
    return { brand }
  }
}
</script>

<style scoped>
</style>
