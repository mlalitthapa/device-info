<template>
  <div class="uk-card uk-card-body">
    <h1 class="uk-card-title">
      {{ device.name }}
    </h1>
    <Specs :specs="device.specs" />
  </div>
</template>

<script>
import Specs from '@/components/device/Specs'

export default {
  name: 'Device',
  components: { Specs },
  props: {
    device: {
      required: true,
      type: Object
    }
  }
}
</script>

<style scoped>
</style>
