<template>
  <div class="uk-flex uk-flex-center">
    <div class="uk-width-2-3">
      <form @submit.prevent="handleSubmit">
        <div class="uk-margin">
          <input v-model="query" class="uk-input" placeholder="Device name or model" type="text">
        </div>
        <div class="uk-margin uk-flex uk-flex-center">
          <button class="uk-button uk-button-secondary">
            Search
          </button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Search',
  props: {
    searched: {
      default: null,
      type: String
    }
  },
  data() {
    return {
      query: this.searched || ''
    }
  },
  methods: {
    handleSubmit() {
      if (!this.query.trim()) return
      this.$router.push(`/search?query=${this.query}`)
    }
  }
}
</script>

<style scoped>
</style>
