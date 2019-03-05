<template>
  <div>
    <table
      v-for="title in titles"
      :key="`spec-${title}`"
      class="uk-table uk-table-responsive uk-table-small uk-table-divider"
    >
      <caption class="uk-text-uppercase uk-text-bold uk-text-primary">
        {{ title }}
      </caption>
      <tbody>
        <tr
          is="spec"
          v-for="(item, index) in specs[title]"
          :key="`spec-item-${index}-${item.name}`"
          :item="item"
        />
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
