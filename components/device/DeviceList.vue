<template>
  <div class="uk-child-width-auto uk-text-center uk-flex uk-flex-center" uk-grid>
    <div v-for="device in devices" :key="device.slug">
      <ListItem :device="device" />
    </div>
  </div>
</template>

<script>
import ListItem from '@/components/device/ListItem'

export default {
  name: 'DeviceList',
  components: { ListItem },
  props: {
    devices: {
      required: true,
      type: Array
    }
  }
}
</script>

<style scoped>
</style>
