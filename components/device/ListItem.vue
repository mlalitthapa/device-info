<template>
  <div class="uk-card uk-card-default">
    <nuxt-link :to="`/device/${device.slug}`" class="uk-link-heading">
      <div class="uk-card-media-top">
        <img :alt="device.image.alt" :src="device.image.src">
      </div>
      <div class="uk-card-body">
        <h3 class="uk-card-title">
          {{ device.name }}
        </h3>
      </div>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  name: 'ListItem',
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
