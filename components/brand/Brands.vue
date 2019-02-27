<template>
  <div class="uk-margin-medium-top">
    <div class="uk-child-width-auto uk-flex uk-flex-center" uk-grid>
      <Brand
        v-for="brand in brands"
        :key="`brand-${brand.slug}`"
        :brand="brand"
      />
    </div>
  </div>
</template>

<script>
import Brand from '@/components/brand/Brand'

export default {
  name: 'Brands',
  components: { Brand },
  props: {
    brands: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
</style>
