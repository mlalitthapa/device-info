<template>
  <div>
    <div class="uk-card uk-card-secondary uk-card-body">
      <h3 class="uk-card-title uk-text-uppercase">
        {{ brand.name }}
      </h3>
      <p>
        {{ brand.devices }}
      </p>
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
