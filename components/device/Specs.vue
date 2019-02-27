<template>
  <div>
    <table
      :key="`spec-${title}`"
      class="uk-table uk-table-responsive uk-table-small uk-table-divider"
      v-for="title in titles"
    >
      <caption class="uk-text-uppercase uk-text-bold uk-text-primary">
        {{ title }}
      </caption>
      <tbody>
        <tr
          v-for="item in specs[title]"
          :item="item"
          :key="`spec-item-${item.name}`"
          is="spec"
        ></tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import Spec from '~/components/device/Spec'

export default {
  name: 'Specs',
  components: { Spec },
  props: {
    specs: {
      required: true,
      type: Object
    }
  },
  computed: {
    titles() {
      return this.specs ? Object.keys(this.specs) : []
    }
  }
}
</script>

<style scoped>
</style>
