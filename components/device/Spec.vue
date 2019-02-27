<template>
  <tr class="uk-text-small">
    <td>
      {{ name }}
    </td>
    <td>
      {{ value }}
    </td>
  </tr>
</template>

<script>
export default {
  name: 'Spec',
  props: {
    item: {
      required: true,
      type: Object
    }
  },
  computed: {
    name() {
      return this.item ? this.item.name : ''
    },
    value() {
      return this.item ? this.item.value : ''
    }
  }
}
</script>

<style scoped>
</style>
