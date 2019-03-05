<template>
  <div>
    <vue-paginate
      v-model="page"
      :click-handler="nextPage"
      :container-class="'uk-pagination uk-flex-center'"
      :next-text="'Next'"
      :page-count="totalPages"
      :prev-text="'Prev'"
      active-class="uk-active"
    />
  </div>
</template>

<script>
export default {
  name: 'Paginate',
  props: {
    pages: {
      default: function() {
        return []
      },
      type: Array
    }
  },
  data() {
    return {
      page: 1
    }
  },
  computed: {
    totalPages() {
      return this.pages.length
    }
  },
  created() {
    const currentPage = this.pages.find(({ link }) => link === '')
    this.page = currentPage.page
  },
  methods: {
    nextPage(tPage) {
      const targetPage = this.pages.find(({ page }) => page === tPage)
      this.$router.push({
        path: `/brand/${targetPage.link}`
      })
    }
  }
}
</script>

<style scoped>
</style>
