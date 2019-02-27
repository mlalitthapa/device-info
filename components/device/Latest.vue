<template>
  <div>
    <h2 class="uk-heading-divider">
      Latest Devices
    </h2>
    <div class="uk-child-width-auto uk-text-center uk-flex uk-flex-center" uk-grid>
      <div v-for="device in devices" :key="device.slug">
        <div class="uk-card uk-card-default">
          <div class="uk-card-media-top">
            <img :alt="device.image.alt" :src="device.image.src">
          </div>
          <div class="uk-card-body">
            <h3 class="uk-card-title">
              {{ device.name }}
            </h3>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Latest',
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
