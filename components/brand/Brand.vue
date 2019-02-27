<template>
  <div>
    <div class="uk-card uk-card-secondary uk-card-body">
      <nuxt-link :to="`/brand/${brand.slug}`" class="uk-link-heading">
        <h3 class="uk-card-title uk-text-uppercase">
          {{ brand.name }}
        </h3>
        <p>
          {{ brand.devices }}
        </p>
      </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Brand',
  props: {
    brand: {
      required: true,
      type: Object
    }
  }
}
</script>

<style scoped>
</style>
